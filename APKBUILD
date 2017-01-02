# Contributor: Shiva Velmurugan <shiv@shiv.me>
# Maintainer: Shiva Velmurugan <shiv@shiv.me>
pkgname=cpputest
pkgver=3.8
pkgrel=1
pkgdesc="CppUTest is a unit testing and mocking framework for C/C++"
url="http://cpputest.github.io/"
arch="all"
license="BSD"
depends=""
makedepends="cmake"
install=""
subpackages="$pkgname-doc"
source="https://github.com/cpputest/${pkgname}/releases/download/v${pkgver}/${pkgname}-${pkgver}.tar.gz"
builddir="$srcdir/$pkgname-$pkgver"

build() {
    cd "$builddir"/cpputest_build
    cmake -DCMAKE_INSTALL_PREFIX:PATH=/usr ..
    make || return 1
}

package() {
    cd "$builddir"
    make DESTDIR="$pkgdir" PREFIX="/usr" install || return 1
    install -Dm644 COPYING "$pkgdir"/usr/share/licenses/$pkgname/COPYING
}

md5sums="e8fdbbb5dd37d32d65919f240f984905  cpputest-3.8.tar.gz"
sha256sums="c81dccc5a1bfc7fc6511590c0a61def5f78e3fb19cb8e1f889d8d3395a476456  cpputest-3.8.tar.gz"
sha512sums="a9592bdc9ffab8b42026ef2010f504e7e37d77fc2f197f89d23f7c9285a101059a0ec66418b914db0383974616d31b26addd1938fb27f45c3e7d9496ed0a0fac  cpputest-3.8.tar.gz"
