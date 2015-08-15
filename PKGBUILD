# Maintainer: Muflone http://www.muflone.com/contacts/english/
# Contributor: yugrotavele <yugrotavele at archlinux dot us>

pkgname=gmtp
pkgver=1.3.8
pkgrel=1
pkgdesc="A simple MP3 player client for MTP based devices"
arch=('i686' 'x86_64')
url="http://gmtp.sourceforge.net/"
license=('BSD')
depends=('flac' 'gtk3' 'libmtp' 'libid3tag' 'libvorbis')
install="${pkgname}.install"
source=("${pkgname}-${pkgver}.tar.gz"::"http://sourceforge.net/projects/gmtp/files/gMTP-${pkgver}/${pkgname}-${pkgver}.tar.gz/download")
sha256sums=('edb9aa6f2421be3090fa53c5384fdf0dfb43cafcf6c1c3621ab5eeb889ebb580')

build() {
  cd "${pkgname}-${pkgver}"
  ./configure --prefix=/usr
  make
}

package() {
  cd "${pkgname}-${pkgver}"
  install -D -m644 COPYING "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
  make DESTDIR="${pkgdir}" install
}
