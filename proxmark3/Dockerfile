FROM debian
MAINTAINER Ronald Huizer <r.huizer@xs4all.nl>

RUN apt-get update && rm -rf /var/lib/apt/lists/*

# Set up the pm3 user and work in his homedir.
RUN     useradd -ms /bin/nologin pm3
USER    pm3
WORKDIR /home/pm3

# Upload and unzip the pm3 zip file.
COPY bin/proxmark3 /home/pm3/proxmark3
ENTRYPOINT ["./proxmark3"]
