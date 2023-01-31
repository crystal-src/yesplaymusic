# Maintainer: Null Talisman <webmaster@raspii.tech>
# Contributor: Qingxu <me@linioi.com>

pkgname=yesplaymusic
pkgver=0.4.7
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
sha256sums=('9b9fc793354e2bcd677b31a7d29e7e5006479fdf7b89c8adfac1e17d072cd2c9'
            'f9e1e23488b9fb10b07ea3d278c1d644f695df118aea460c0521988a5f012162')

package() {
    install -d "${pkgdir}/usr/share/applications"
    cp -r "${srcdir}/usr/share/icons" "${pkgdir}/usr/share/icons"
    install -Dm644 -t "${pkgdir}/usr/share/applications" "${srcdir}/yesplaymusic.desktop"
    install -Dm644 -t "${pkgdir}/usr/lib/${pkgname}" "${srcdir}/opt/YesPlayMusic/resources/app.asar"
}
