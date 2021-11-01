you can define x-containers in ~/.config/socle.yml
example :
``` yaml
myFirst: |
  bash -c 'mkdir -p /tmp/empty ; cd /tmp/empty ; docker build --build-arg NOCACHE=$(date +%s) -t toto/myfirst . -f -<<<$(curl -L  https://gitlab.com/dockerimagesforsocle/imageswithi3/-/raw/main/myFirst.build)  && docker run -d --name $NAME  --privileged -v /var/run/dbus:/var/run/dbus --shm-size=2gb -v /tmp/.X11-unix:/tmp/.X11-unix:ro -v /dev/snd:/dev/snd -v /sys/fs/cgroup:/sys/fs/cgroup:ro    toto/myfirst'
```

x-containers are special containers with windows managers,
[here](https://gitlab.com/containers-for-socle) are the container images i use

[:fontawesome-solid-paper-plane: myFirst](https://gitlab.com/containers-for-socle/i3-101/dockerfiles/-/blob/main/i3-101.build){ .md-button .md-button--primary }

- debian buster
- i3
- polybar
- wezterm
- chromium
