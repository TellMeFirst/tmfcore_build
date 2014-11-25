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

## How this repository is organized

The `tmfcore_build_cli` directory (which is also a git submodule) contains
the code needed to build TMF's core as a command line application. More
information on this module can be found in the [related git
repository](https://github.com/bassosimone/tmfcore_build_cli).

The `tmfcore_build_war` directory (which is also a git submodule) contains the
code needed to build TMF's core as a Java [Web application ARchive
(WAR)](https://en.wikipedia.org/wiki/WAR_%28file_format%29) that can be
runnable inside a container (e.g., Tomcat, Jetty-runner). More
information on this module can be found in the [related git
repository](https://github.com/bassosimone/tmfcore_build_war).
