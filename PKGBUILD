# Contributor: dibblethewrecker <dibblethewrecker.at.jiwe.org>

pkgname=gquilt
pkgver=0.24
pkgrel=1
pkgdesc='A PyGTK GUI wrapper for quilt'
arch=('any')
url='http://gquilt.sourceforge.net/'
license=('GPL2')
depends=('quilt' 'pygtk')
source=(
  "http://downloads.sourceforge.net/sourceforge/${pkgname}/${pkgname}-${pkgver}.tar.gz"
  
  # Tarball is missing gquilt.xpm and repository seems to be missing 0.24
  # completely, so take it from 0.23
  "http://${pkgname}.hg.sourceforge.net/hgweb/${pkgname}/${pkgname}/raw-file/RELEASE_0_23/gquilt.xpm"
)
md5sums=(
  '7199e01eea24c9c52259df2e9d6299d9'
  'ca932f2bca024a7a53b8105cf0509f94'
)

build() {
  cd ${pkgname}-${pkgver}
  cp ../gquilt.xpm .
}

package() {
  cd ${pkgname}-${pkgver}

  python2 setup.py install --root="${pkgdir}"
  desktop-file-install gquilt.desktop --dir "${pkgdir}/usr/share/applications"
}
