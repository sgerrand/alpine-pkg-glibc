# Maintainer: Glider Labs <team@gliderlabs.com>

pkgname="glibc"
pkgver="2.21"
pkgrel="2"
pkgdesc="GNU C Library compatibility layer"
arch="x86_64"
url="https://github.com/gliderlabs/alpine-glibc"
license="GPL"
install="$pkgname.post-install"
source="http://mirrors.kernel.org/archlinux/core/os/x86_64/glibc-${pkgver}-${pkgrel}-${arch}.pkg.tar.xz
ld.so.conf"
subpackages="$pkgname-bin"
depends="!libgcc"

package() {
  mkdir -p "$pkgdir"/usr/glibc
  mkdir "$pkgdir"/etc
  mkdir "$pkgdir"/lib64
  cp -a "$srcdir"/usr "$pkgdir"/usr/glibc/usr
  cp -a "$srcdir"/ld.so.conf "$pkgdir"/etc/
  rm -rf "$pkgdir"/usr/glibc/usr/lib/systemd \
    "$pkgdir"/usr/glibc/usr/lib/gconv \
    "$pkgdir"/usr/glibc/usr/lib/locale \
    "$pkgdir"/usr/glibc/usr/lib/tmpfiles.d \
    "$pkgdir"/usr/glibc/usr/lib/getconf \
    "$pkgdir"/usr/glibc/usr/lib/audit \
    "$pkgdir"/usr/glibc/usr/lib/*.a \
    "$pkgdir"/usr/glibc/usr/bin/* \
    "$pkgdir"/usr/glibc/usr/include \
    "$pkgdir"/usr/glibc/usr/share
  cp -a "$srcdir"/usr/bin/ldconfig "$pkgdir"/usr/glibc/usr/bin/
  ln -s /usr/glibc/usr/lib/ld-linux-x86-64.so.2 ${pkgdir}/lib64/ld-linux-x86-64.so.2
}

bin() {
  mkdir -p "$subpkgdir"/usr/glibc/usr/bin
  cp -a "$srcdir"/usr/bin/* "$subpkgdir"/usr/glibc/usr/bin/
  rm "$subpkgdir"/usr/glibc/usr/bin/ldconfig
}

md5sums="cd2bef93120db7401bd7a4451e97dab4  glibc-2.21-2-x86_64.pkg.tar.xz
fda27293b95f89c7a61a0d379d1c3bde  ld.so.conf"
