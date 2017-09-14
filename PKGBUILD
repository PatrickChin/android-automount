# Maintainer: François-Xavier Thomas <fx.thomas+arch@gmail.com>
pkgname=android-automount
pkgver=0.1
pkgrel=1
pkgdesc="Adds udev rules to automount Android devices"
arch=('any')
url="https://github.com/fxthomas/android-automount"
license=('unknown')
depends=(go-mtpfs-git daemonize)
source=('99-android-mtp.rules' 'android-mtp@.service' 'android-mtp')
md5sums=('6e5ec25f6deb769abb6dd87c2b8fb1b8'
         '08629c5e48a72b2e49f5eccd6db0e150'
         'e85830e4b8575cbd2ad7d20accdbffbb')
install='android-automount.install'

package() {
  mkdir -p $pkgdir/usr/lib/udev/rules.d/
  mkdir -p $pkgdir/usr/lib/systemd/system/
  mkdir -p $pkgdir/usr/bin/
  install -Dm644 $srcdir/99-android-mtp.rules $pkgdir/usr/lib/udev/rules.d/99-android-mtp.rules
  install -Dm644 $srcdir/android-mtp@.service $pkgdir/usr/lib/systemd/system/android-mtp@.service
  install -Dm755 android-mtp $pkgdir/usr/bin/android-mtp
}

# vim:set ts=2 sw=2 et:
