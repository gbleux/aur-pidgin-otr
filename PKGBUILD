pkgname=pidgin-otr
pkgver=4.0.0
pkgrel=1
pkgdesc='Off-the-Record Messaging plugin for Pidgin and Finch.'
arch=('i686' 'x86_64')
license=('GPL')
url='http://www.cypherpunks.ca/otr/'
depends=('libotr>=4.0.0' 'pidgin' 'perlxml' 'git')
makedepends=('automake')
source=("https://otr.cypherpunks.ca/${pkgname}-${pkgver}.tar.gz")
md5sums=('eadb953376acc474e56041d4c12aa2c8')

build() {
  cd "$srcdir/${pkgname}-${pkgver}"
  ./configure --prefix=/usr && make
}

package() {
  cd "$srcdir/${pkgname}-${pkgver}"
  make DESTDIR="${pkgdir}" install
}
