# tor-shadow.docker

Base Docker image for simulating/emulating Tor using Shadow.

Just run `make all` to build the image. Once you have the image, then
```bash
docker run -it --tmpfs /dev/shm:rw,nosuid,nodev,exec,size=1g tor-shadow
```
will run the image.
The `--tmpfs` argument is important. Probably you must increase the `size` 
parameter.

There are more things that you might need to change. See [the shadow 
documentation][shadow-doc].

[shadow-doc]: https://github.com/shadow/shadow/blob/main/docs/1.1-Shadow.md#system-configs-and-limits

The Git repo of the tools are located in `/tor-shadow`.

