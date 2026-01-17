## Podman Utils

The repository contains useful utils for podman. Currently it consists of a single one.

### Podman Port Forward

So I was always wondering, why can I forward a port from a random container in k8s, but I cannot on my home server with podman? I read some articles which mentioned some crazy commands involving `slirp4netns`, `pasta`, `netavark` and many other things which I don't need to know about and I don't want ot know about (beyond knowing the fact that redhat willy-nilly replaces one implementation with the other).

With a little help of google I was able to build from sticks and glue a simple tool which just forwards a port from any container. That's it.

Behold!

`podman-fwd <local_host:port> <target_container> <remote_host:port>`

Not a perfect syntax, but useful. Enjoy.

This works fine with docker too. 

This scripts requires `socat` installed.
