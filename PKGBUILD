# This is an example PKGBUILD file. Use this as a start to creating your own,
# and remove these comments. For more information, see 'man PKGBUILD'.
# NOTE: Please fill out the license field for your package! If it is unknown,
# then please put 'unknown'.

# Maintainer: Adison Trueblood <adisontrueblood3@gmail.com>
pkgname=Augur
pkgver=V1.0
pkgrel=1
epoch=
pkgdesc="Taint Analysis"
arch=()
url="https://www.github.com/nuprl/augur"
license=('UPL-1.0')
groups=(sudo)
depends=()
makedepends=()
checkdepends=()
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
source=("$pkgname-$pkgver.tar.gz"
        "$pkgname-$pkgver.patch")
noextract=()
md5sums=()
validpgpkeys=()

prepare() {
        cd "$pkgname-$pkgver"
        patch -p1 -i "$srcdir/$pkgname-$pkgver.patch"
}

build() {
        cd "$pkgname-$pkgver"
        ./configure --prefix=/usr
        make
}


check() {
        cd "$pkgname-$pkgver"
        make -k check
}

package() {
        cd "$pkgname-$pkgver"
        make DESTDIR="$pkgdir/" install
}



