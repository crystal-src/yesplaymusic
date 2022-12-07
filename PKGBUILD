# Maintainer: Null Talisman <webmaster@raspii.tech>
# Contributor: Qingxu <me@linioi.com>

pkgname=yesplaymusic
pkgver=0.4.5
pkgrel=1
pkgdesc="A third party music application for Netease Music"
arch=("x86_64")
url="https://github.com/qier222/YesPlayMusic"
license=("MIT")
provides=("yesplaymusic")
depends=(
    "electron19"
)
optdepends=(
    'libnotify'
    'libappindicator-gtk3'
)
source=(
    "YesPlayMusic-${pkgver}.pacman::https://github.com/qier222/YesPlayMusic/releases/download/v${pkgver}${subver}/YesPlayMusic-${pkgver}${subver}.pacman"
    "yesplaymusic.desktop"
)
sha256sums=('77bc47093cf5f954f8f08fe22e91a9d0dc2d8d8414f85c092126edb9fbec26e5'
            'cfbb79c471f5ae1010e17c8abc1f4decb738a8214138b9b703e8d8239d56fc15')

package() {
    install -d "${pkgdir}/usr/share/applications"
    cp -r "${srcdir}/usr/share/icons" "${pkgdir}/usr/share/icons"
    install -Dm644 "${srcdir}/yesplaymusic.desktop" "${pkgdir}/usr/share/applications/${pkgname}.desktop"
    install -Dm644 "${srcdir}/opt/YesPlayMusic/resources/app.asar" "${pkgdir}/usr/share/${pkgname}/${pkgname}.asar"
}
