# Maintainer: Nicky726 (Nicky726 <at> gmail <dot> com)
# Contributor: Panagiotis Papadopoulos (pano_90 <at> gmx <dot> net)

pkgname=partionmonitor
_name=partmon
pkgver=1.0
pkgrel=2
pkgdesc="KDE Logging/Monitoring: The program displays accesses to files and directories.."
arch=('i686' 'x86_64')
url="http://kde-apps.org/content/show.php/PartionMonitor?content=153264&PHPSESSID=cd822adbb82d731e11bf7e9fba54e459"
license=('GPL')
depends=('kdebase-runtime>=4.7' 'kdelibs>=4.7' 'qt4' 'linux>=2.6.38')
makedepends=('cmake' 'gettext' 'automoc4')
options=('!libtool')
source=(http://kde-apps.org/CONTENT/content-files/153264-$_name.tar.bz2)
sha1sums=('b8c66de98c16d2e0eb1e7702a04d4b8ee62877e1')

build() {
  cd "${srcdir}/$pkgname"
  mkdir build && cd build
  cmake -DCMAKE_INSTALL_PREFIX=/usr .. && make -j3

  make DESTDIR="${pkgdir}" install
  cd .. && rm -rf build
}

