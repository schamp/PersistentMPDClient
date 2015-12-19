# PersistentMPDClient

Provides an auto-reconnecting client wrapper around a python-mpd2 (https://github.com/Mic92/python-mpd2/) MPDClient class object.

Will intercept every command to the MPDClient and attempt to ping the server to determine if the client is still connected.
If not, will reconnect before finally attempting to invoke the requested command.

Relieves python-mpd2 applications of the burden of checking for disconnection and reconnecting.
