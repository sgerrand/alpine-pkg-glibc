FROM alpine:3.1
RUN apk -U add wget ca-certificates
RUN mkdir -p /tmp/opt \
  && wget http://mirrors.kernel.org/archlinux/core/os/x86_64/glibc-2.21-2-x86_64.pkg.tar.xz -qO- \
  | tar -C /tmp/opt -xJf -
RUN /tmp/opt/usr/bin/ldconfig -C /ld.so.cache -r /tmp /opt/usr/lib
