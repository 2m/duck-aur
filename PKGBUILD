# Maintainer: Michael Corrigan <ghost.vonage AT gmail DOT com>
# Upstream URL: https://duck.sh/

pkgname=duck
pkgver=5.0.2.20424
pkgrel=1
pkgdesc="Cyberduck CLI"
PKGEXT='.pkg.tar'
arch=('x86_64' 'i686')
license=('GPL')
options=(!strip)
url="https://duck.sh/"
makedepends=('rpmextract')
depends=('java-runtime')
md5sums_x86_64=('2517850cef1d7f7a84633148e2cd4ec3')
md5sums_i686=('b60006cad3bb169a6968e2ed3b431656')
source_x86_64=("https://repo.cyberduck.io/stable/x86_64/duck-${pkgver}.x86_64.rpm")
source_i686=("https://repo.cyberduck.io/stable/i386/duck-${pkgver}.i686.rpm")

package() {
  rpmextract.sh *
  chmod -R g-w opt
  mv opt "${pkgdir}"
  mkdir -p "${pkgdir}/usr/bin"
  ln -s /opt/duck/duck "${pkgdir}/usr/bin/duck"
}
