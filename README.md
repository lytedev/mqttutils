# mqttutils

A few simple utilities for recording and playing back MQTT messages.


## Dependencies

**NOTE**: WIP

* Automake (`pacman -S automake`)
* Mosquitto (`pacman -S mosquitto`)


## Compile

**NOTE**: WIP

```
./configure
make
```


## Documentation

Coming... probably never, let's be honest.

You can see the documentation for the original project here:
http://der-b.com/2014-04-26/mqtt-developing-tools/

The primary additions are a `-P` or `--password` option and a `-u` or
`--username` option for authentication via
[`mosquitto_username_pw_set`][auth_func_ref].


## Examples

Below are some examples showing basic usage.


### Recording

`./src/mqttrecorder -t gpsupdates/# -b brokerhostname -p 1883 -u client -P secret -v ~/output.log`


### Playback

`./src/mqttplayer -b brokerhostname -p 1883 -u client -P secret -v ~/output.log`


[auth_func_ref]: https://mosquitto.org/api/files/mosquitto-h.html#mosquitto_username_pw_set
