pkgname=orchis-gtk
﻿_pkgname=orchis-gtk-theme
pkgver=2.0.0
pkgrel=1
pkgdesc="Orchis is a modern GTK3 theme for Linux."
arch=('any')
url="https://github.com/snwh/orchis-gtk-theme"
license=('GPL3')
depends=(gtk-engine-murrine)
makedepends=('git')
optdepends=()
provides=('orchis-gtk')
conflicts=('orchis-gtk')
source=('git://github.com/snwh/orchis-gtk-theme.git')
md5sums=('SKIP')

pkgver() {
  cd $srcdir/$_pkgname
  echo $(git rev-list --count HEAD).$(git rev-parse --short HEAD)
}

package() {

  # create theme dirs
  install -d -m 755 "$pkgdir"/usr/share/themes/Orchis
  install -d -m 755 "$pkgdir"/usr/share/themes/Orchis-Dark

  # install theme
  cd $srcdir/orchis-gtk-theme/Orchis
  cp -r . "$pkgdir"/usr/share/themes/Orchis/
  cd $srcdir/moka-gtk-theme/Orchis-Dark
  cp -r . "$pkgdir"/usr/share/themes/Orchis-Dark/
}
