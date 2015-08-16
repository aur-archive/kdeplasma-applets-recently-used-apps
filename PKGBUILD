# Maintainer: Carl Mueller  archlinux at carlm e4ward com

pkgname=kdeplasma-applets-recently-used-apps
pkgver=0.2
pkgrel=2
pkgdesc="Plasmoid to show recently used applications"
arch=(i686 x86_64)
url="http://kde-look.org/content/show.php/Recently+used+applications?content=152344"
license=('GPL')
depends=('kdebase-workspace')
makedepends=('cmake' 'automoc4')
source=(http://www.kde-look.org/CONTENT/content-files/152344-plasma-applet-recentlyusedapps-$pkgver.tar.bz2)
md5sums=('e1d3697b914e1e0e476377994bc28158')
build() {
  cd $srcdir/plasma-applet-recentlyusedapps/
  mkdir build
  cd build
  cmake -DQT_QMAKE_EXECUTABLE=qmake-qt4 -DCMAKE_BUILD_TYPE=Release -DCMAKE_INSTALL_PREFIX=`kde4-config --prefix` ..
  make
  make DESTDIR=$pkgdir install
}
