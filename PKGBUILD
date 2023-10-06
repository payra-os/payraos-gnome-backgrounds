# Maintainer: dr460nf1r3 <dr460nf1r3 at garudalinux dot org>

pkgname=payraos-gnome-backgrounds
pkgver=1.0.0
pkgrel=1
pkgdesc="Payra OS wallpaper collection"
arch=('any')
url="https://github.com/payra-os/$pkgname"
license=('GPLv3')
makedepends=('git')
source=("git+https://github.com/payra-os/payraos-gnome-backgrounds.git")
sha256sums=('SKIP')

pkgver() {
	cd "$srcdir/$pkgname"
	printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"

}

package() {
    cd ${pkgname}
    install -d ${pkgdir}/usr/share/backgrounds/$pkgname
    cp -r src/$pkgname/* ${pkgdir}/usr/share/backgrounds/$pkgname
    install -d ${pkgdir}/usr/share/gnome-background-properties
    cp -r src/$pkgname/*.xml ${pkgdir}/usr/share/gnome-background-properties/payraos-gnome-backgrounds.xml
}

