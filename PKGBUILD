
pkgname=ogre
pkgver=1.9.0
_pkgver=1-9
_commit=sinbad-ogre-55e89ae88219
pkgrel=1
pkgdesc='Scene-oriented, flexible 3D engine written in C++'
arch=('x86_64')
url='http://www.ogre3d.org'
license=('custom:MIT')
depends=('boost-libs' 'freeimage' 'freetype2' 'libxaw' 'libxrandr'
         'nvidia-cg-toolkit' 'zziplib' 'ois' 'glu' 'tinyxml')
makedepends=('boost' 'cmake' 'ttf-dejavu' 'mesa')
source=("https://bitbucket.org/sinbad/ogre/get/v${_pkgver}.tar.gz")
md5sums=('bc72f80d2e7da53e51c400e9fa357be4')
 
build() {
  mkdir build 
  cd build
 
  cmake ../${_commit} \
    -DCMAKE_INSTALL_PREFIX=/usr \
    -DOGRE_LIB_DIRECTORY=/usr/lib \
    -DCMAKE_BUILD_TYPE=Release
 
  make
}
 
package() {
  cd build
 
  make DESTDIR=${pkgdir} install
 
}