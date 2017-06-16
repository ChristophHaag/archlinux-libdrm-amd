# $Id$
# Maintainer: Jan de Groot <jgc@archlinux.org>
# Maintainer: Clément Guérin <geecko.dev@free.fr>

pkgname=libdrm-amd
_pkgname=libdrm
pkgver=2.4.14.1612.g1fe5f0fe
pkgrel=1
pkgdesc="Userspace interface to kernel DRM services with AMDGPU-PRO additions"
arch=(i686 x86_64)
license=('custom')
depends=('libpciaccess')
makedepends=('valgrind' 'xorg-util-macros' 'libxslt' 'docbook-xsl')
checkdepends=('cairo')
provides=('libdrm' 'libdrm-git')
conflicts=('libdrm' 'libdrm-git')
replaces=('libdrm-new' 'libdrm-nouveau')
url="http://dri.freedesktop.org/"
source=(git://people.freedesktop.org/~agd5f/drm#branch=amd-mainline-hybrid-master20170517)
md5sums=('SKIP')

pkgver() {
        cd 'drm'
        git describe --always | sed 's|libdrm.||g;s|-|.|g'
}

prepare() {
  cd drm

  # pthread is useless in Linux
  sed -i 's/PKG_CHECK_MODULES(PTHREADSTUBS, pthread-stubs)//' configure.ac
}

build() {
  cd drm
  ./autogen.sh --prefix=/usr \
              --enable-udev \
              --enable-intel \
              --enable-radeon \
              --enable-nouveau \
              --enable-vmwgfx
  make
}

check() {
  cd drm
  # make -k check
}

package() {
  cd drm
  make DESTDIR="$pkgdir" install
  #install -m755 -d "$pkgdir/usr/share/licenses/$_pkgname"
  #install -m644 ../COPYING "$pkgdir/usr/share/licenses/$_pkgname/"
}
