# Maintainer: Gerald Dachs <gda[at]dachsweb[dot]de>
pkgname=png++
pkgver=0.2.5
pkgrel=1yavdr1
license=('custom')
pkgdesc="a C++ wrapper for libpng"
arch=('i686' 'x86_64')
url="http://savannah.nongnu.org/projects/pngpp/"
depends=('libpng' 'doxygen')
source=(http://download.savannah.gnu.org/releases/pngpp/$pkgname-$pkgver.tar.gz)
md5sums=('beb02ba7daddcf847e1617e75b7af567')

build() {
  mkdir -p "${pkgdir}/usr/include" || return 1
  mkdir -p "${pkgdir}/usr/share/doc" || return 1
  mkdir -p "${pkgdir}/usr/share/licenses/${pkgname}" || return 1
  cd $srcdir/$pkgname-$pkgver
  make docs || return 1
  make install PREFIX="${pkgdir}/usr" || return 1
}

package() {
  cd $srcdir/$pkgname-$pkgver
  cp -f COPYING ${pkgdir}/usr/share/licenses/$pkgname
}
