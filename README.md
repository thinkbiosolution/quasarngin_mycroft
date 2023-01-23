
## About 
QuasaR-NGIN 5G & Edge cloud connectivity to enable real-time
communication with healthcare provided in events like stroke and fall events.

## Examples 
* “Quasar I am having a stroke”
* “Quasar Help”. “I am having a stroke”
* “Quasar Help”. “John is having a stroke”
* “Quasar Help”. “I think John is having a stroke”
* “Quasar I fell down”
* “Quasar Help”. “I fell down and can not get up”
* “Quasar Help”. “John is fell down”
* “Quasar Help”. “John fell down and I think he cannot get up”
* “Quasar call an ambulance”

# Setup

## Install MycroftAI

### Install Ubuntu 22.04 LTS

See [Installing Ubuntu](https://ubuntu.com/tutorials/install-ubuntu-desktop#1-overview "Installing Ubuntu")

### Install Dependencies

```
sudo apt-get update
sudo apt-get install -y alsa pulseaudio
```

### Install MycroftAI engine

The simplest way to install Mycroft for Linux is to clone the mycroft-core repo to your system and run a shell script, which will install all dependencies, and Mycroft components.
The mycroft-core repo is at https://github.com/MycroftAI/mycroft-core.
The instructions below will install Mycroft in your HOME directory.

```
git clone https://github.com/MycroftAI/mycroft-core.git
cd mycroft-core
./dev_setup.sh -fm
```

The `dev_setup.sh` script identifies, installs and configures dependencies that Mycroft needs to run.
The script will also install and configure virtualenv. virtualenv is a tool to create isolated Python environments. It is a way to isolate an application - in this case Mycroft - from other applications. It helps to better manage both dependencies and security.
If you are running a Linux distribution other than Ubuntu, Debian, Arch or Fedora, you may need to manually install packages as instructed by `dev_setup.sh`.

### Pair device to MycroftAI account

* Create a Mycroft account and sign in on the device you have installed the platform on.

* Install Mycroft Skills, which are add-ons that provide additional functionality to the Mycroft AI platform. You can find and install skills through the Mycroft Skills Marketplace.

* Configure the device's microphone and speaker settings. Mycroft AI uses these to listen and speak.

### Running this skill

#### Add Quasar-NGIN skill to local MycroftAI environment

Clone this repository to the `skills` subfolder in your local `mycroft-core` working folder 

#### Running MycroftAI

The Mycroft for Linux installation includes two scripts that you use to control Mycroft services.
start-mycroft.sh
start-mycroft.sh is used to start one, or all, Mycroft services. This script uses the virtualenv created by dev_setup.sh.
The usage of start-mycroft.sh is:
``` 
usage: start-mycroft.sh [command] [params]
```

Once everything is set up, you can begin using Mycroft AI by saying "Hey Mycroft" and giving it commands or asking it questions.
 
#### Running Quasar-NGIN skill
Once MycroftAI is setup and running, and you have installed this skill, say 
“Quasar I am having a stroke”. The system will send a message to a server that logs and reports emergency events so that emergency services can respond appropriately.