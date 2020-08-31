# Contributor: Shiva Velmurugan <shiv@shiv.me>
# Maintainer: Shiva Velmurugan <shiv@shiv.me>
pkgname=cpputest
pkgver=4.0
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
    cd "$builddir"
    cmake -DCMAKE_INSTALL_PREFIX:PATH=/usr $srcdir/
    make || return 1
}

package() {
    cd "$builddir"
    make DESTDIR="$pkgdir" PREFIX="/usr" install || return 1
    install -Dm644 COPYING "$pkgdir"/usr/share/licenses/$pkgname/COPYING
}

md5sums="d41d8cd98f00b204e9800998ecf8427e cpputest-4.0.tar.gz"
sha256sums="e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 cpputest-4.0.tar.gz"
sha512sums="cf83e1357eefb8bdf1542850d66d8007d620e4050b5715dc83f4a921d36ce9ce47d0d13c5d85f2b0ff8318d2877eec2f63b931bd47417a81a538327af927da3e cpputest-4.0.tar.gz"
