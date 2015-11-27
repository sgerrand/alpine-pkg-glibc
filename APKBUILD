# Maintainer: Glider Labs <team@gliderlabs.com>

pkgname="glibc"
pkgver="2.22"
pkgrel="5"
pkgdesc="GNU C Library compatibility layer"
arch="x86_64"
url="https://github.com/gliderlabs/alpine-glibc"
license="GPL"
source="https://github.com/andyshinn/docker-glibc-builder/releases/download/$pkgver-$pkgrel/glibc-bin-$pkgver-$pkgrel-x86_64.tar.gz"
subpackages="$pkgname-bin"

package() {
  mkdir -p "$pkgdir"
  cp -a "$srcdir"/usr "$pkgdir"
  rm "$pkgdir"/usr/glibc-compat/etc/rpc
  rm -rf "$pkgdir"/usr/glibc-compat/bin
  rm -rf "$pkgdir"/usr/glibc-compat/sbin
  rm -rf "$pkgdir"/usr/glibc-compat/lib/gconv
  rm -rf "$pkgdir"/usr/glibc-compat/lib/getconf
  rm -rf "$pkgdir"/usr/glibc-compat/lib/audit
  rm -rf "$pkgdir"/usr/glibc-compat/lib/*.a
  rm -rf "$pkgdir"/usr/glibc-compat/include
  rm -rf "$pkgdir"/usr/glibc-compat/share
  rm -rf "$pkgdir"/usr/glibc-compat/var
  #ln -s /usr/glibc-compat/usr/lib/ld-linux-x86-64.so.2 ${pkgdir}/lib64/ld-linux-x86-64.so.2
}

bin() {
  mkdir -p "$subpkgdir"/usr/glibc-compat
  cp -a "$srcdir"/usr/glibc-compat/bin "$subpkgdir"/usr/glibc-compat
  cp -a "$srcdir"/usr/glibc-compat/sbin "$subpkgdir"/usr/glibc-compat
}

md5sums="4f2ea9f8cc1be716479f831597a14682  glibc-bin-2.22-5-x86_64.tar.gz"
