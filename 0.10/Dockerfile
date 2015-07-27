#      __//
#     /.__.\
#     \ \/ /
#  '__/    \
#   \-      )
#    \_____/
# _____|_|____
#      " "
#   crossy.io

FROM crossyio/qemu-rpi:latest

MAINTAINER Crossy.IO <docker@crossy.io>

RUN proot -0 -b /etc/resolv.conf -r /opt/rootfs -q qemu-arm-static /bin/bash -c \
  'curl http://node-arm.herokuapp.com/node_0.10.36_armhf.deb -o /tmp/node_0.10.36_armhf.deb && dpkg -i /tmp/node_0.10.36_armhf.deb'

RUN proot -0 -b /etc/resolv.conf -r /opt/rootfs -q qemu-arm-static /bin/bash -c \
  'curl -L https://npmjs.org/install.sh | sh'
