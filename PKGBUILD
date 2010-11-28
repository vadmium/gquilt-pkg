# Contributor: dibblethewrecker <dibblethewrecker.at.jiwe.org>

pkgname=gquilt
pkgver=0.24
pkgrel=2
pkgdesc='A PyGTK GUI wrapper for quilt'
arch=('any')
url='http://gquilt.sourceforge.net/'
license=('GPL2')
depends=('quilt' 'pygtk')
source=("http://downloads.sourceforge.net/sourceforge/${pkgname}/${pkgname}-${pkgver}.tar.gz")
md5sums=('7199e01eea24c9c52259df2e9d6299d9')

package() {
  cd ${pkgname}-${pkgver}

  python2 setup.py install --root="${pkgdir}"
  desktop-file-install gquilt.desktop --dir "${pkgdir}/usr/share/applications"
}
