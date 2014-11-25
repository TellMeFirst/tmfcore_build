# TMFCoreBuild

This repository contains the subrepositories needed to build the
[core module](https://github.com/bassosimone/tmfcore) of
[TellMeFirst (TMF)](http://tellmefirst.polito.it/) both as
a command-line application and as a Java Web Archive (aka WAR).

## How to clone this repository

Since this repository contains submodules, to clone this you have to
run the following command:

    git clone --recursive https://github.com/bassosimone/tmfcore_build

Otherwise, if you have already cloned, you can fetch the submodules using
the following command:

    git submodule update --init

## Dependencies

We use [maven](http://maven.apache.org/) to build and clean the code,
so you need to install it. This repository also assumes that you use
[Java8](https://jdk8.java.net/). So, you need to install Java8 as well.

On Xubuntu 14.04, you can install all the above packages by running
the following command:

    sudo apt-get install maven openjdk-8-jdk

We also develop using [NetBeans](https://netbeans.org/), therefore, you
may also want to install it (but other editors/IDEs are fine as well).
Since we use Java8, if you want to use NetBeans, you need to download and
install NetBeans8 from the [NetBeans web site](https://netbeans.org/).

## How to build and clean the code

Once you have installed all the dependencies, you can build the
code using the following command:

    mvn package

You can instead clean the compiled artifacts using:

    mvn clean

To combine both (recommended to be sure that the compile process
starts from scratch) do:

    mvn clean package

## How this repository is organized

The top-level
[pom.xml](https://github.com/bassosimone/tmfcore_build/blob/master/pom.xml)
file references two modules: `tmfcore_build_cli` and `tmfcore_build_war`.

The `tmfcore_build_cli` module (which is also a git submodule) contains
the code needed to build TMF's core as a command line application. More
information on this module can be found in the [related git
repository](https://github.com/bassosimone/tmfcore_build_cli).

The `tmfcore_war` module (which is also a git submodule) contains the
code needed to build TMF's core as a Java [Web application ARchive
(WAR)](https://en.wikipedia.org/wiki/WAR_%28file_format%29) that can be
runnable inside a container (e.g., Tomcat, Jetty-runner). More
information on this module can be found in the [related git
repository](https://github.com/bassosimone/tmfcore_build_war).
