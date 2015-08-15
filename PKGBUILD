# Maintainer: AlexanderR <alexander r at gmx com>
# Contributor: Eric Forgeot < http://ifiction.free.fr >
pkgname=fizmo
pkgver=0.7.9
pkgrel=1
pkgdesc="A Z-Machine interpreter supporting unicode, sound, blorbfile and more."
arch=(i686 x86_64)
url="http://spellbreaker.org/~chrender/fizmo/"
license=('BSD')
depends=('libxml2' 'libsndfile' 'libjpeg-turbo' 'libpng' 'sdl')
groups=('inform')
source=(http://spellbreaker.org/~chrender/fizmo/source/$pkgname-$pkgver.tar.gz)
md5sums=('4b36df277d5ca7a8517ac02ab4d42347')

build() {
  cd $pkgname-$pkgver

  ./configure --prefix=/usr
  make
}
  
package() {
  cd $pkgname-$pkgver

  make DESTDIR="$pkgdir" install
  install -Dm644 COPYRIGHT.txt "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}

