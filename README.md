# Charybdis IRC Daemon in Docker
The Charybdis IRC daemon running on docker. This is installed to /irc in the container,
so it is expected you pass /irc/etc as a host folder volume and store your config
and SSL certs in there. PID file is set to go to /irc/ircd.pid in case the container
gets forcibly terminated (persistent PID doesn't get cleaned up, so putting it there
ensures it doesn't exist again when container is restarted).

It is expected everything is running/owned as user 1000.
