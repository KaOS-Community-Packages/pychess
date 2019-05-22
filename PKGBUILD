pkgname=pychess
pkgver=1.0.0
pkgrel=1
pkgdesc='Chess client'
arch=('x86_64')
url='http://pychess.org/'
license=('GPL')
depends=('python3-gobject3' 'python3-psutil' 'python3-cairo' 'python3-sqlalchemy' 'python3-pexpect' 'python3-ptyprocess' 'python3-websockets' 'gtksourceview3' 'gst-plugins-base' 'desktop-file-utils' 'adwaita-icon-theme' 'sqlite' 'stockfish')
makedepends=('git' 'python3-pexpect' 'python3-ptyprocess')
optdepends=('gnuchess: a chess engine for graphical chess frontends')
install=pychess.install
source=("https://github.com/pychess/pychess/releases/download/$pkgver/${pkgname}-$pkgver.tar.gz")
md5sums=('99cf00d7092303df0265759d0789d72e')

package() {
  cd "${pkgname}-$pkgver"
  python3 setup.py install --prefix=/usr --root=$pkgdir

  # FS#59882
  find "$pkgdir" -wholename "external/pexpect" -type d -delete
}
