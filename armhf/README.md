### Dockerized i2pd for Raspberry Pi.

Before build docker image you should create swap partiotion (if you don't use swap before)

    # dd if=/dev/zero of=/swap bs=1024 count=524288
    # mkswap /swap 
    # swapon /swap

Create image (can take some time)

    $ docker build --rm -t i2pd .

Run image in container

    $ docker run --detach=true -p 7070:7070 -p 4446:4446 -v /home/pi/docker/i2pd/share:/mnt --name i2pd i2pd

Delete swap partition

    # swapoff /swap 
    # rm /swap 

Exposed ports

* 2827 — BOB
* 4446 — eepSite proxy
* 6668 — Irc2P proxy
* 7650 — I2PControl
* 7655 — SAM (UDP)
* 7656 — SAM (TCP)
* 7070 — Web interface