# Contributor: Markus Martin <markus@archwyrm.net>
pkgname=yaml-cpp
pkgver=0.2.7
pkgrel=1
pkgdesc="YAML parser and emitter in C++, written around the YAML 1.2 spec"
url="http://code.google.com/p/yaml-cpp/"
arch=('i686' 'x86_64')
license=('MIT')
makedepends=('cmake')
source=(http://yaml-cpp.googlecode.com/files/$pkgname-$pkgver.tar.gz)
md5sums=('6878e14bad90c69a8f2caca273eb24c2')

build() {
    cd $startdir/src/$pkgname

    cmake . -DCMAKE_INSTALL_PREFIX=/usr -DYAML_CPP_BUILD_TOOLS=0 || return 1
    make || return 1
    make DESTDIR=$startdir/pkg install || return 1
}
