# Maintainer: Jaroslav Lichtblau <dragonlord@aur.archlinux.org>
# Contributor: Paolo "PalmaWay" Palmieri <palmaway@gmx.it>

pkgname=man2html
pkgver=3.0.1
pkgrel=2
pkgdesc="A Unix manpage-to-HTML converter"
arch=('i686' 'x86_64')
url="http://www.oac.uci.edu/indiv/ehood/man2html.html"
license=('GPL')
depends=('man')
makedepends=('perl')
source=(http://www.oac.uci.edu/indiv/ehood/tar/$pkgname$pkgver.tar.gz)
md5sums=('1c0d28c83225d0ebc845f2386c8f8384')

build() {
  cd ${srcdir}/${pkgname}${pkgver}

  install -d ${pkgdir}/usr/bin ${pkgdir}/usr/share/man/man1 || return 1
  perl install.me -batch -binpath ${pkgdir}/usr/bin -manpath ${pkgdir}/usr/share/man || return 1
}
