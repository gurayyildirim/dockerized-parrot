# dockerized-parrot
Dockerized version of Parrot GNU/Linux.

- It is tested with low configuration machines (even with 512 MB ram with 1vCPU it runs well!).
- You can run it in seconds after pulling the image. You can remove it in seconds as well. No installation is required other than Docker.
- You can have Dockerized Parrot GNU/Linux command line in only one command.
- You can build your images based on these images with your preferred tools and versions.
- Multiple instances can be run in the same time with minimal resource usage.

![Screenshot of Dockerized Parrot](screenshot.png)

## Usage
If you do not have Docker, you can install it with:
```
curl -sSL https://get.docker.com | sh
```
Note that you should not pipe codes from web without understanding what it does, so it is recommended to read, understand and execute or try other installation methods from Docker website.

Basic usage of pre-builded 'headless' image (runs latest version):
```
docker run -it guray/dockerized-parrot
```

## Different Versions
There are three versions, all available from Docker Hub or you can build your own:
- Core Only
- Headless
- Standard
Image size increases to downwards on the list.

Images are tagged with their latest build with their names. So you can use them directly with these commands:
```
docker run -it guray/dockerized-parrot:coreonly
docker run -it guray/dockerized-parrot:headless
docker run -it guray/dockerized-parrot:standard
```

## Old Versions and Tags
Different tags and old versions can be accessed from Docker Hub page for `dockerized-parrot` repo. You can reach the repo from [Docker Hub Repository Link](https://hub.docker.com/r/guray/dockerized-parrot/ "here").

## Minimal Image
Core only image is minimal, but does not include lots of useful packages. It is suitable for creating your own image with your favourite tools.

Headless image and standard image includes many tools. Headless has 'parrot-pico' package while standard image includes 'parrot-tools' package.


If you want to build from stratch and run:
```
cd standard
docker build -t guray/dockerized-parrot:0.1-standard .
docker run -it guray/dockerized-parrot:0.1-standard
```

If you want to use host system's network, just add `--network host` in command:
```
docker run -it --network host guray/dockerized-parrot
```

Also, you may want to remove container when it is exited:
```
docker run -it --rm guray/dockerized-parrot
```

## Donation
ETH: 0x26e13f0a138d6c6214466612ba10e1bf7ec4ce06
BTC: 1M2oS8DtavqomUmcXkbeXF4sZ84f4RMAPq


