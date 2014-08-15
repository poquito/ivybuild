# poquito ivybuild

a build system for JavaEE artifacts based on [ant](http://ant.apache.org/) and [ivy](http://ant.apache.org/ivy/)

## Installation

###  Preconditions
To run ivybuild you need to provide [ant](http://ant.apache.org/) 1.8.4 ore above on your system. 

The project contains a `build.xml` which will install and setup the build system.

The default location for the installation will be the folder `ivybuild` inside the default ivy directory (e.g. $HOME/.ivy2). 


###  Install or Update from Binary Release
You can download the latest release (e.g. ivybuild-1.0.0.zip) from the [poquito repository](http://poquito.at/ivyrepo/milestone/at/poquito/ivybuild) and unzip the File in any temporary directory.

Open a console (cmd.exe or any unix shell) and run the build script. 

The following sample, shows how you can install ivybuild from a command line.

    # download current release from repository
    > curl -O http://poquito.at/ivyrepo/milestone/at/poquito/ivybuild/1.0.0/ivybuild-1.0.0.zip
    
    # unzip into temporary directory tmp
    > unzip ivybuild-1.0.0.zip -d tmp
    
    # change into temporary directory
    > cd ivybuild
    
    # run ant build
    > ant


###  Install or Update from github repository
You can download and install the latest release from the [github repository](https://github.com/poquito/ivybuild.git): 

Open a console (cmd.exe or any unix shell) and type the following commands:


    # clone the repository
    > git clone https://github.com/poquito/ivybuild.git
    
    # change into project dir
    > cd ivybuild/at.poquito.ivybuild
    
    # run ant build
    > ant

### Console Setup
`ivybuild` needs a few configuration properties for succesfull execution. With the first run of the installation script, a `build.properties` file has been created in the `$HOME/.ivy2` directory. This file contains the default configuration and you have to add it to your `ANT_ARGS` environment-variable. Subsequent installations or updates will not destroy your current configuraiton.

    # on windows
    set ANT_ARGS="-propertyfile %HOMEPATH%/.ivy2/build.properties
    
    # on unix
    export ANT_ARGS="-propertyfile ~/.ivy2/build.properties

