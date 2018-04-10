
![](https://user-images.githubusercontent.com/260/38534678-61701e56-3c4d-11e8-95d5-163c095e9ad0.png)

A super easy way to get started with [Magic Cards](https://github.com/maddox/magic-cards).


## Magic Cards

[Magic Cards](https://github.com/maddox/magic-cards) is a fun project that merges the physical world with the digital world. This repo is your one stop shop to getting it set up as easy as possible.

Clone down this repo, edit your configurations, and you'll be up and running with Magic Cards and Sonos immediately.

## Getting Started

Read more about Magic Cards in its [documentation](https://github.com/maddox/magic-cards/tree/master/docs).

### Prerequisites

This is expected to run on a Raspberry Pi. You should have git and docker already installed. You will also need to install `docker-compose` to get everything running easily.

#### Install Docker

Installing Docker is as easy as a couple of commands:

```bash
curl -sSL https://get.docker.com/ | sh
```

Once it's installed, run this command so your `pi` user can use Docker.

```bash
sudo usermod -G docker pi
```

Log out of your Pi and back in so your user has permissions to use Docker.

#### Install docker-compose

You'll need to use the `pip3` python package manager to install `docker-compose` to ensure you get the right version for your Raspberry Pi.

```bash
sudo pip3 install docker-compose
```

Let it go through it's paces and you should be ready to go.


## Installing
Installing is as easy as:

1. Clone down this repo
1. Edit the appropriate config files
1. Start it up

### Clone & Set Up Configs

Clone down the repo.

    git clone git@github.com:maddox/magic-cards-docker.git

Edit the `config.json` and `actions.json` files found in:

`magic-cards/config`

Learn about configuring Magic Cards in its [documentation](https://github.com/maddox/magic-cards/blob/master/docs/install.md#configure).

This repo already has a Sonos action ready and configured. You should edit the `actions.json` file to change the room name you want your Sonos action to happen on. The room name is case sensitive.

### Start It Up

Launch the containers with:

    script/start

This will launch everything and keep it up. Browse the `script` dir to see other
things you can use.

## Access Services

You can access the services on these ports:

1. Magic Cards: port 5000
1. Node Sonos HTTP API: port 5005
