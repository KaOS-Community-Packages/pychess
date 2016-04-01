pkgname=pychess
pkgver=0.12.3
pkgrel=1
pkgdesc='Chess client'
arch=('x86_64')
url='http://pychess.org/'
license=('GPL')
depends=('python2-gobject' 'python2-cairo' 'gtksourceview3' 'gst-plugins-base' 'desktop-file-utils')
install=pychess.install
source=("http://www.pychess.org/download/${pkgname}-$pkgver.tar.gz")
md5sums=('70035ee3523f7d1c182137a9e146050c')

package() {
  cd "${pkgname}-$pkgver"
  python setup.py install --prefix=/usr --root=$pkgdir
}
