# Maintainer: Antony Ho <ntonyworkshop@gmail.com>
pkgname=pycangjie
pkgver=0.0.1
pkgrel=1
pkgdesc="This is a Python wrapper to libcangjie, the library implementing Cangjie and Quick input methods."
arch=('x86_64' 'i686')
url="https://github.com/bochecha/pycangjie"
license=('LGPL3')
depends=('libcangjie' 'python>=3.2')
makedepends=('cython>=0.17')
replaces=('pycangjie-git')
sha1sums=('SKIP')
source=("http://ibus-cangjie.opensource.hk/downloads/$pkgname/cangjie-$pkgver.tar.xz")

check() {
  cd "$srcdir/cangjie-$pkgver"
  make check
}

build() {
  cd "$srcdir/cangjie-$pkgver"
  ./configure --prefix=/usr
  make
}

package() {
  cd "$srcdir/cangjie-$pkgver"
  make DESTDIR="$pkgdir/" install
}
