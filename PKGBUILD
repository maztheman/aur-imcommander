# Maintainer: Your Name <youremail@domain.com>
pkgname="ImCommander"
pkgver="0.0.3"
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
source=("${pkgname}-v${pkgver}.tar.gz::${url}/archive/refs/tags/v${pkgver}.tar.gz")
noextract=()
sha256sums=('e038bbe9c1781dfcb844aae70eeda4eaadcf5fe5f61e0b503397f97d72d68899')

build() {
  cd "$pkgname-$pkgver"
  cmake -B build -S . -GNinja -DCMAKE_INSTALL_PREFIX=/usr -DImCommander_ENABLE_HARDENING=OFF -DImCommander_ENABLE_CLANG_TIDY=OFF -DImCommander_ENABLE_CPPCHECK=OFF -DImCommander_ENABLE_GLOBAL_HARDENING=OFF
  cmake --build build --config RelWithDebInfo
}

package() {
  cd "$pkgname-$pkgver"
  cmake --install build --prefix "$pkgdir/usr"
}
