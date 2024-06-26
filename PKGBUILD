# Maintainer: Your Name <youremail@domain.com>
pkgname="imcommander"
pkgver="0.0.2"
pkgrel="1"
pkgdesc="Split file manager using ImGui"
arch=("any")
url="https://github.com/maztheman/${pkgname}"
license=('MIT')
groups=()
depends=()
makedepends=("cmake" "ninja" "gcc" "git" "python3")
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
source=("${pkgname}-v${pkgver}.tar.gz::${url}/archive/refs/tags/${pkgver}.tar.gz")
noextract=()
sha256sums=('215e1a44576f3f767417ed8989b6597cfbe2465308882efd65204834dd2db367')

build() {
  cd "$pkgname-$pkgver"
  cmake -B build -S . -GNinja -DCMAKE_INSTALL_PREFIX=/usr
  cmake --build build
}

package() {
  cd "$pkgname-$pkgver"
  cmake --install build --prefix "$pkgdir/usr"
}
