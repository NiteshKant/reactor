# Reactor

`Reactor` is a foundational library building for reactive fast data applications on the JVM. It provides abstractions for Java, Groovy and other JVM languages to make building event and data-driven applications easier. It’s also really fast. On a recent laptop with a dual-core processor, it's possible to process over 15,000,000 events per second with the `RingBufferDispatcher` and over 25,000,000 events per second in a single thread. Other dispatchers are available to provide the developer with a range of choices from thread-pool style, long-running task execution to non-blocking, high-volume task dispatching.

[![Build Status](https://drone.io/github.com/reactor/reactor/status.png)](https://drone.io/github.com/reactor/reactor/latest)

### Build instructions

`Reactor` uses a Gradle-based build system. Building the code yourself should be a straightforward case of:

    git clone git@github.com:reactor/reactor.git
    cd reactor
    ./gradlew test

This should cause the submodules to be compiled and the tests to be run. To install these artifacts to your local Maven repo, use the handly Gradle Maven plugin:

    ./gradlew install

### Maven Artifacts

Snapshot Maven artifacts are provided in the SpringSource snapshot repositories. To add this repo to your Gradle build, specify the URL like the following:

    ext {
      reactorVersion = '2.0.0.RC1'
    }

    repositories {
      maven { url 'http://repo.spring.io/libs-release' }
      //maven { url 'http://repo.spring.io/libs-milestone' }
      //maven { url 'http://repo.spring.io/libs-snapshot' }
      mavenCentral()
    }

    dependencies {
      // Reactor Core
      compile 'io.projectreactor:reactor-core:$reactorVersion'
      // Reactor Groovy
      //compile 'io.projectreactor:reactor-groovy:$reactorVersion'
      // Reactor Spring
      //compile 'io.projectreactor:reactor-spring:$reactorVersion'
    }

### Documentation

* [Guides](https://github.com/reactor/reactor/wiki)
* [API Reference](http://reactor.github.io/docs/api/)

### Community / Support

* [reactor-framework Google Group](https://groups.google.com/forum/?#!forum/reactor-framework)
* [GitHub Issues](https://github.com/reactor/reactor/issues)

### License

Reactor is [Apache 2.0 licensed](http://www.apache.org/licenses/LICENSE-2.0.html).
