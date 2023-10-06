# Maintainer: E5H4N <m.eshan@outlook.in>

pkgname=payraos-gnome-backgrounds
pkgver=1.0.0
pkgrel=1
pkgdesc="Payra OS wallpaper collection"
arch=('any')
url="https://github.com/payra-os/$pkgname"
license=('GPLv3')
makedepends=('git')
source=("git+https://github.com/payra-os/$pkgname.git")
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

