# Maintainer: Glider Labs <team@gliderlabs.com>

pkgname="glibc"
pkgver="2.22"
_pkgrel="5"
pkgrel="7"
pkgdesc="GNU C Library compatibility layer"
arch="x86_64"
url="https://github.com/gliderlabs/alpine-glibc"
license="GPL"
source="https://github.com/andyshinn/docker-glibc-builder/releases/download/$pkgver-$_pkgrel/glibc-bin-$pkgver-$_pkgrel-x86_64.tar.gz
nsswitch.conf"
subpackages="$pkgname-bin $pkgname-i18n"

package() {
  mkdir -p "$pkgdir/lib64" "$pkgdir/usr/glibc-compat/lib/locale" "$pkgdir"/etc
  cp -a "$srcdir"/usr "$pkgdir"
  cp -a "$srcdir"/nsswitch.conf "$pkgdir"/etc/nsswitch.conf
  touch "$pkgdir"/usr/glibc-compat/etc/ld.so.conf
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
  ln -s /usr/glibc-compat/lib/ld-linux-x86-64.so.2 ${pkgdir}/lib64/ld-linux-x86-64.so.2
}

bin() {
  depends="$pkgname"
  mkdir -p "$subpkgdir"/usr/glibc-compat
  cp -a "$srcdir"/usr/glibc-compat/bin "$subpkgdir"/usr/glibc-compat
  cp -a "$srcdir"/usr/glibc-compat/sbin "$subpkgdir"/usr/glibc-compat
}

i18n() {
  depends="$pkgname-bin"
  arch="noarch"
  mkdir -p "$subpkgdir"/usr/glibc-compat
  cp -a "$srcdir"/usr/glibc-compat/share "$subpkgdir"/usr/glibc-compat
}

md5sums="4f2ea9f8cc1be716479f831597a14682  glibc-bin-2.22-5-x86_64.tar.gz
5be984273de4203318c9c3fb0d4e9d2b  nsswitch.conf"
