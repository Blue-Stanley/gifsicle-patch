# $Id: PKGBUILD 192181 2013-08-06 18:35:21Z eric $
# Maintainer: Eric Bélanger <eric@archlinux.org>

pkgname=gifsicle
pkgver=1.71
pkgrel=1
pkgdesc="A powerful command-line program for creating, editing, manipulating and getting information about GIF images and animations"
arch=('i686' 'x86_64')
url="http://www.lcdf.org/gifsicle/"
license=('GPL')
depends=('libx11')
source=(http://www.lcdf.org/${pkgname}/${pkgname}-${pkgver}.tar.gz
        gifview-root.patch)
sha1sums=('a7665faa99b157ea545b65761d19e15b9b4a8b74'
          '8bbe1ea0d584759015b6c990941a417d60cba332')

build() {
  cd ${pkgname}-${pkgver}
  patch -Np1 -i ../gifview-root.patch
  ./configure --prefix=/usr
  make
}

package() {
  cd ${pkgname}-${pkgver}
  make DESTDIR="${pkgdir}" install
}

