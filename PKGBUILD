# Archtrack maintainer: Evan Teitelman <teitelmanevan at gmail dot com>
# Contributor: Francesco Piccinno <stack.box@gmail.com>

pkgname=iaxflood
pkgver=latest
pkgrel=1
pkgdesc="IAX flooder"
url="http://www.hackingexposedvoip.com/"
makedepends=('gcc' 'make')
depends=('glibc')
license=('GPL')
arch=(i686 x86_64)
source=(http://www.hackingexposedvoip.com/tools/${pkgname}.tar.gz)
md5sums=('39d557dcfdcab7c668ba321f4de82664')

groups=(archtrack archtrack-sniffing-spoofing archtrack-stress-testing)

build() {
  cd "$srcdir/$pkgname"
  sed -i "s:gcc :gcc $CFLAGS :" makefile || return 1
  make || return 1
  install -Dm755 $pkgname $pkgdir/usr/bin/$pkgname || return 1
}

