# Traffic Light Control Plugin #

## Introduction ##

This gazebo plugin supplied a way to control traffic light via network.
The plugin will start a server during the startup which will listen for control via internet.
A client may send commands to server to control traffic lights in the simulator.

## How to use ##

### build ###

```{bash}
cd plugin
mkdir build
cd build
cmake ..
make
```

Then add the following line into your startup file (`~/.bashrc` or `~/.zshrc` or etc.)
(Not required if you are using the startup script)

```{bash}
export GAZEBO_PLUGIN_PATH=:/path/to/build:${GAZEBO_PLUGIN_PATH}
```

### load the plugin

Append the following line into the world section in your world file.

```{xml}
<plugin name="TrafficLightController" filename="libTrafficLightController.so"></plugin>
```
---

## Protocol

This plugin is using a text protocol.
User may use commands to control traffic lights.
Each command must be separated by a newline character.
A command is a traffic light model name in gazebo followed by the color it required to be changed.
The model name and color in one command should separate by a single space character.


The formal definition of the protocol as follow.

```
NEWLINE = "\n"
SPACE = " "
identifier = {any gazebo valid model name which should not containing space or newline}
color = red | yellow | green
COMMAND = identifier SPACE color NEWLINE
```

After each command is handled by server, the server will return an "OK\n".

## Known issue

- There is no error handling right now, to be specific User may not know if a command was executed successfully.
- The server listening address and port is hardcoded to 127.0.0.1:23456.
- Only "stop_light_post'" model from gazebo official repository supported.

## Examples to control the traffic lights (using netcat for debug purpose) ##
- Open a new terminal
- Type "nc 127.0.0.1 23456"
- Type "stop_light_post_170 red"
- Type "stop_light_post_170 green"
- Type "stop_light_post_170 yellow"
