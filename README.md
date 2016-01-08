# juno

An OS X launch agent for Jupyter Notebook

# Requirements

* Jupyter Notebook installed

# Installation

Either fork n' clone or clone juno:

    git clone git@github.com:versionzero/juno.git

Create the required directories:

    mkdir -p ~/Library/LaunchAgents/
    mkdir -p /usr/local/var/jupyter
    mkdir -p /usr/local/var/ipyparallel

Copy the scripts in to place:

    cp src/jupyter/jupyter.plist ~/Library/LaunchAgents/
    cp src/ipyparallel/ipyparallel.plist ~/Library/LaunchAgents/
    cp src/jupyter/jupyter /usr/local/bin
    cp src/ipyparallel/ipyparallel /usr/local/bin
    chmod 755 /usr/local/bin/jupyter
    chmod 755 /usr/local/bin/ipyparallel

Launch the agents:

    launchctl load ~/Library/LaunchAgents/jupyter.plist
    launchctl load ~/Library/LaunchAgents/ipyparallel.plist
