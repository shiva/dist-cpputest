# Contributor: Shiva Velmurugan <shiv@shiv.me>
# Maintainer: Shiva Velmurugan <shiv@shiv.me>
pkgname=cpputest
pkgver=3.8
pkgrel=1
pkgdesc="CppUTest is a unit testing and mocking framework for C/C++"
url="http://cpputest.github.io/"
arch="all"
license="Custom"
depends=""
makedepends=""
install=""
subpackages="$pkgname-dev $pkgname-doc"
source="https://github.com/cpputest/${pkgname}/releases/download/v${pkgver}/${pkgname}-${pkgver}.tar.gz"
builddir="$srcdir/$pkgname-$pkgver"

build() {
	cd "$builddir"
	autoreconf ${srcdir}/ -i
  ./${srcdir}/configure
  make
}

package() {
	cd "$builddir"
	# make DESTDIR="$pkgdir" PREFIX="/usr" install || return 1
}

