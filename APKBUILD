# Maintainer: Glider Labs <team@gliderlabs.com>

pkgname="glibc-compat"
pkgver=2.21
pkgrel=2
pkgdesc="GNU C Library compatibility layer"
arch="x86_64"
url="https://github.com/gliderlabs/alpine-glibc-compat"
license="GPL"
depends=""
makedepends=""
source="http://mirrors.kernel.org/archlinux/core/os/x86_64/glibc-${pkgver}-${pkgrel}-${arch}.pkg.tar.xz
ld.so.cache"

package() {
  install -dm755 ${pkgdir}/usr/glibc/lib
  install -dm755 ${pkgdir}/etc
  install -dm755 ${pkgdir}/lib64
  
  install -m644 ${srcdir}/ld.so.cache ${pkgdir}/etc/ld.so.cache
  
  install -m755 ${srcdir}/usr/lib/ld-2.21.so ${pkgdir}/usr/glibc/lib/ld-2.21.so
  install -m755 ${srcdir}/usr/lib/ld-2.21.so ${pkgdir}/lib64/ld.so
  install -m755 ${srcdir}/usr/lib/libBrokenLocale-2.21.so ${pkgdir}/usr/glibc/lib/libBrokenLocale-2.21.so
  install -m755 ${srcdir}/usr/lib/libSegFault.so ${pkgdir}/usr/glibc/lib/libSegFault.so
  install -m755 ${srcdir}/usr/lib/libanl-2.21.so ${pkgdir}/usr/glibc/lib/libanl-2.21.so
  install -m755 ${srcdir}/usr/lib/libc-2.21.so ${pkgdir}/usr/glibc/lib/libc-2.21.so
  install -m755 ${srcdir}/usr/lib/libc.so ${pkgdir}/usr/glibc/lib/libc.so
  install -m755 ${srcdir}/usr/lib/libcidn-2.21.so ${pkgdir}/usr/glibc/lib/libcidn-2.21.so
  install -m755 ${srcdir}/usr/lib/libcrypt-2.21.so ${pkgdir}/usr/glibc/lib/libcrypt-2.21.so
  install -m755 ${srcdir}/usr/lib/libdl-2.21.so ${pkgdir}/usr/glibc/lib/libdl-2.21.so
  install -m755 ${srcdir}/usr/lib/libm-2.21.so ${pkgdir}/usr/glibc/lib/libm-2.21.so
  install -m755 ${srcdir}/usr/lib/libmemusage.so ${pkgdir}/usr/glibc/lib/libmemusage.so
  install -m755 ${srcdir}/usr/lib/libnsl-2.21.so ${pkgdir}/usr/glibc/lib/libnsl-2.21.so
  install -m755 ${srcdir}/usr/lib/libnss_compat-2.21.so ${pkgdir}/usr/glibc/lib/libnss_compat-2.21.so
  install -m755 ${srcdir}/usr/lib/libnss_db-2.21.so ${pkgdir}/usr/glibc/lib/libnss_db-2.21.so
  install -m755 ${srcdir}/usr/lib/libnss_dns-2.21.so ${pkgdir}/usr/glibc/lib/libnss_dns-2.21.so
  install -m755 ${srcdir}/usr/lib/libnss_files-2.21.so ${pkgdir}/usr/glibc/lib/libnss_files-2.21.so
  install -m755 ${srcdir}/usr/lib/libnss_hesiod-2.21.so ${pkgdir}/usr/glibc/lib/libnss_hesiod-2.21.so
  install -m755 ${srcdir}/usr/lib/libnss_nis-2.21.so ${pkgdir}/usr/glibc/lib/libnss_nis-2.21.so
  install -m755 ${srcdir}/usr/lib/libnss_nisplus-2.21.so ${pkgdir}/usr/glibc/lib/libnss_nisplus-2.21.so
  install -m755 ${srcdir}/usr/lib/libpcprofile.so ${pkgdir}/usr/glibc/lib/libpcprofile.so
  install -m755 ${srcdir}/usr/lib/libpthread-2.21.so ${pkgdir}/usr/glibc/lib/libpthread-2.21.so
  install -m755 ${srcdir}/usr/lib/libpthread.so ${pkgdir}/usr/glibc/lib/libpthread.so
  install -m755 ${srcdir}/usr/lib/libresolv-2.21.so ${pkgdir}/usr/glibc/lib/libresolv-2.21.so
  install -m755 ${srcdir}/usr/lib/librt-2.21.so ${pkgdir}/usr/glibc/lib/librt-2.21.so
  install -m755 ${srcdir}/usr/lib/libthread_db-1.0.so ${pkgdir}/usr/glibc/lib/libthread_db-1.0.so
  install -m755 ${srcdir}/usr/lib/libutil-2.21.so ${pkgdir}/usr/glibc/lib/libutil-2.21.so


  # Symlinks
  cd ${pkgdir}/usr/glibc/lib
  ln -s ld-2.21.so ld-linux-x86-64.so.2
  ln -s libBrokenLocale-2.21.so libBrokenLocale.so
  ln -s libBrokenLocale-2.21.so libBrokenLocale.so.1
  ln -s libanl-2.21.so libanl.so
  ln -s libanl-2.21.so libanl.so.1
  ln -s libc-2.21.so libc.so.6
  ln -s libcidn-2.21.so libcidn.so
  ln -s libcidn-2.21.so libcidn.so.1
  ln -s libcrypt-2.21.so libcrypt.so
  ln -s libcrypt-2.21.so libcrypt.so.1
  ln -s libdl-2.21.so libdl.so
  ln -s libdl-2.21.so libdl.so.2
  ln -s libm-2.21.so libm.so
  ln -s libm-2.21.so libm.so.6
  ln -s libnsl-2.21.so libnsl.so
  ln -s libnsl-2.21.so libnsl.so.1
  ln -s libnss_compat-2.21.so libnss_compat.so
  ln -s libnss_compat-2.21.so libnss_compat.so.2
  ln -s libnss_db-2.21.so libnss_db.so
  ln -s libnss_db-2.21.so libnss_db.so.2
  ln -s libnss_dns-2.21.so libnss_dns.so
  ln -s libnss_dns-2.21.so libnss_dns.so.2
  ln -s libnss_files-2.21.so libnss_files.so
  ln -s libnss_files-2.21.so libnss_files.so.2
  ln -s libnss_hesiod-2.21.so libnss_hesiod.so
  ln -s libnss_hesiod-2.21.so libnss_hesiod.so.2
  ln -s libnss_nis-2.21.so libnss_nis.so
  ln -s libnss_nis-2.21.so libnss_nis.so.2
  ln -s libnss_nisplus-2.21.so libnss_nisplus.so
  ln -s libnss_nisplus-2.21.so libnss_nisplus.so.2
  ln -s libpthread-2.21.so libpthread.so.0
  ln -s libresolv-2.21.so libresolv.so
  ln -s libresolv-2.21.so libresolv.so.2
  ln -s librt-2.21.so librt.so
  ln -s librt-2.21.so librt.so.1
  ln -s libthread_db-1.0.so libthread_db.so
  ln -s libthread_db-1.0.so libthread_db.so.1
  ln -s libutil-2.21.so libutil.so
  ln -s libutil-2.21.so libutil.so.1
}

md5sums="cd2bef93120db7401bd7a4451e97dab4  glibc-2.21-2-x86_64.pkg.tar.xz
9afdab705a861a109453ad164e915254  ld.so.cache"
