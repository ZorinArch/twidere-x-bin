# Maintainer: ZorinArch
# Contributor: ZorinArch

_pkgname=twidere-x
pkgname="${_pkgname}-bin"
pkgver=1.6.0
pkgrel=1
pkgdesc="Next generation of Twidere for Android"
arch=('x86_64')
url="https://github.com/TwidereProject/TwidereX-Android"
license=('GPL')
source=("$url/releases/download/v$pkgver/${_pkgname}_$pkgver-1_amd64.deb")
sha256sums=('7ba1a0ac1c8ce33d60cb3182c55affb4c065803c561cd9784c9c7e65fcdf694a')

package() {
	cd $srcdir
	tar -xf data.tar.xz -C $pkgdir
	install -Dm644 $pkgdir/opt/twidere-x/lib/twidere-x-Twidere_X.desktop $pkgdir/usr/share/applications/twidere-x.desktop
	install -Dm644 $pkgdir/opt/twidere-x/lib/Twidere_X.png $pkgdir/usr/share/pixmaps/Twidere_X.png
	install -d $pkgdir/usr/bin/
	ln -s '/opt/twidere-x/bin/Twidere X' $pkgdir/usr/bin/$_pkgname
}

