# Maintainer: Clark Steven <ckenthtb@gmail.com>
pkgname='dwm'
pkgver=1
pkgrel=1
pkgdesc="Clark's dwm build"
arch=('x86_64')
url="https://github.com/learkedins/dwm"
license=('GPL')
depends=('libx11' 'git' 'libxft' 'libxinerama' 'freetype2' 'fontconfig')
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
