Steam on Docker
===============
This repository contains files and helper scripts to build a Docker container capable of running Steam for Linux.

It does this by providing access to certain files necessary for forwarding containerized graphical applications.
## How to use
Try this concise one-liner: ```cd steam-on-linux && ./build && ./run```

In case of emergency, don't panic! Try ```./login``` and run ```steam``` from within the container.
This can often reveal very important debugging information, or, in some cases, spam completely useless walls of text.

## Common issues
1. Graphics drivers

Disparate driver versions can cause major problems if no open source alternatives exist.

In this case, the appropriate host equivalent driver must be manually added and installed via the Dockerfile.
The important thing to remember with proprietary drivers is that both the host and container *must use the exact same driver version*.

2. Game support

Not all games will run. Why? Who knows! It is usually up to game developers to ensure their code doesn't break on uncommon environments.
While Source 1 games should be supported, there is no guarantee that they will always work.
This may be due to future updates either to Source engine games or Docker itself.
