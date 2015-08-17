# Contributor: Aleix Pol <aleixpol@kde.org>

pkgname=qlalr
pkgver=20120313
pkgrel=1
pkgdesc="Qt LALR parser generator"
arch=('any')
url="http://labs.trolltech.com/page/Projects/Compilers/QLALR"
license=('GPL')
depends=('qt>=4.2.0')
makedepends=('git')
provides=('qlalr')
conflicts=()
source=()
md5sums=()

_gitrepo="git://gitorious.org/qt/qlalr.git"
_svnname="qlalr"

build() {
  cd "$srcdir"
  if [ -d ${pkgname} ]; then
    rm -rf ${pkgname}
  fi
  git clone ${_gitrepo}
  cd ${pkgname}/src

  qmake || return 1
  make -j3 || return 1
  
  mkdir -p $pkgdir/usr/bin
  install qlalr -t $pkgdir/usr/bin
} 
