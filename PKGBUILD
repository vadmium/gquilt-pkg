# $Id: PKGBUILD,v 1.4 2008/10/28 14:42:59 abhidg Exp $
# Contributor: dibblethewrecker <dibblethewrecker.at.jiwe.org>

pkgname=gquilt
pkgver=0.20
pkgrel=1
pkgdesc="A PyGTK GUI wrapper for quilt"
arch=('i686' 'x86_64')
url="http://users.bigpond.net.au/Peter-Williams/"
license=('GPL2')
depends=('quilt' 'pygtk')
source=(http://downloads.sourceforge.net/sourceforge/gquilt/$pkgname-$pkgver.tar.gz)
md5sums=('6e80efd284ece0dd73205dcd65793a8d')

build() {
  cd $startdir/src/$pkgname-$pkgver
  sed -i "s|PREFIX=/usr/local|PREFIX=/usr|g" Makefile
  make || return 1
  make DESTDIR=$startdir/pkg install
}
