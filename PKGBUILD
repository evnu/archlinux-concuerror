# Maintainer: Magnus Mueller <mamuelle@informatik.hu-berlin.de>

pkgname=concuerror-git
pkgver=0.0.0
pkgrel=1
pkgdesc="Concuerror is a systematic testing tool for concurrent Erlang programs"
arch=('i686' 'x86_64')
url="https://github.com/mariachris/Concuerror"
license=('BSD')
depends=('pacman' 'erlang')
makedepends=('git' 'make')
provides=('concuerror')
source=("$pkgname"::'git://github.com/mariachris/Concuerror.git')
# Because the sources are not static, skip Git checksum:
md5sums=('SKIP')

pkgver() {
  cd "$srcdir/$pkgname"
  # Use the tag of the last commit
  git describe --long | sed -E 's/([^-]*-g)/r\1/;s/-/./g'
}

build() {
  cd "$srcdir/$pkgname"
  make
}

package() {
  cd "$srcdir/$pkgname"
}
