# Maintainer: TBK <aur at jjtc dot eu>
# Contributor: TBK <aur at jjtc dot eu>

pkgname=atools
pkgver=19.0.3
pkgrel=1
pkgdesc='APKBUILD and aports linter for Alpine Linux'
url='https://gitlab.alpinelinux.org/Leo/atools'
arch=('x86_64')
license=('MIT')
makedepends=('scdoc' 'redo-c')
checkdepends=('bats-core')
source=("$pkgname-$pkgver.tar.gz::https://gitlab.alpinelinux.org/Leo/atools/-/archive/$pkgver/atools-$pkgver.tar.gz") 
sha256sums=('ce4312fa86f72b3344b84c01e70d4bc1da36b015a22c4c83250906445d46408a')
_builddir="$pkgname-$pkgver"

build() {
	cd "$_builddir"
	redo build
}

check() {
	cd "$_builddir"
	redo check
}

package() {
	cd "$_builddir"
	DESTDIR="$pkgdir" redo install
}
