FROM ubuntu:20.04
RUN apt-get update && apt-get install -y python3 sudo bash ca-certificates iproute2 curl && apt-get clean;
RUN rm /bin/sh && ln -s /bin/bash /bin/sh
RUN sudo curl https://apt.releases.teleport.dev/gpg -o /usr/share/keyrings/teleport-archive-keyring.asc && source /etc/os-release && echo "deb [signed-by=/usr/share/keyrings/teleport-archive-keyring.asc] \
https://apt.releases.teleport.dev/${ID?} ${VERSION_CODENAME?} stable/v12" \
| sudo tee /etc/apt/sources.list.d/teleport.list > /dev/null && apt-get update && apt-get install teleport=12.1.5 && apt-get clean
