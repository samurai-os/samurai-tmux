# This is an example PKGBUILD file. Use this as a start to creating your own,
# and remove these comments. For more information, see 'man PKGBUILD'.
# NOTE: Please fill out the license field for your package! If it is unknown,
# then please put 'unknown'.

# Maintainer: Paul Buzakov <paulbuzakov@gmail.com>
pkgname=samurai-tmux
pkgver=0.1.0.beta.r2.g2136c4c
pkgrel=1
epoch=
pkgdesc="TMUX config for SamuraiOS DevTeam Linux"
arch=("x86_64")
url="https://github.com/samurai-os/samurai-tmux.git"
license=("ISC")
groups=()
depends=(tmux)
makedepends=(git)
checkdepends=()
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
source=("git+$url")
noextract=()
sha256sums=("SKIP")
validpgpkeys=()

pkgver() {
  cd "$pkgname"
  git describe --long --abbrev=7 | sed 's/^v//;s/\([^-]*-g\)/r\1/;s/-/./g'
}

package() {
  mkdir -p "${pkgdir}/etc"
  cp "${srcdir}/${pkgname}/etc/tmux.conf" "${pkgdir}/etc/tmux.conf"
}
