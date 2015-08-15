# Maintainer: tuftedocelot@silenceisdefeat.com
pkgname=dswitcher
pkgver=6
pkgrel=2
pkgdesc='Dmenu-based window switcher for EWHM-compliant X11 window managers'
arch=('i686' 'x86_64')
url="https://github.com/Antithesisx/dswitcher"
license='GPLv3'
depends=('wmctrl' 'dmenu')
makedepends=('git')
source=("git://github.com/Antithesisx/dswitcher.git")
md5sums=('SKIP') #generate with 'makepkg -g'

pkgver() {
    cd "$srcdir/$pkgname"
    git rev-list --count HEAD
}

package() {
    install -Dm 755 "$srcdir/$pkgname/$pkgname" "${pkgdir}/usr/bin/$pkgname"
    install -D -m644 "$srcdir/$pkgname/LICENSE" "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}
