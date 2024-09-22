# This is an example PKGBUILD file. Use this as a start to creating your own,
# and remove these comments. For more information, see 'man PKGBUILD'.
# NOTE: Please fill out the license field for your package! If it is unknown,
# then please put 'unknown'.

# Maintainer: Paul Buzakov <paulbuzakov@gmail.com>
pkgname=samurai-tmux
pkgver=0.1.0.beta.r1.g84f3c0a
pkgrel=1
epoch=
pkgdesc="TMUX config for SamuraiOS DevTeam Linux"
arch=('x86_64')
url="https://github.com/samurai-os/samurai-tmux"
license=('ISC')
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
source=('git+https://github.com/samurai-os/samurai-tmux.git#branch=main')
noextract=()
sha256sums=("SKIP")
validpgpkeys=()

pkgver() {
  cd "$pkgname"
  git describe --long --abbrev=7 | sed 's/^v//;s/\([^-]*-g\)/r\1/;s/-/./g'
}

package() {
  mkdir -p "${pkgdir}/etc"
  cp "${srcdir}/etc/tmux.conf" "${pkgdir}/etc/tmux.conf"
}
