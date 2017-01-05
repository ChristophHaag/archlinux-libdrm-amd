# $Id$
# Maintainer: Jan de Groot <jgc@archlinux.org>

pkgname=libdrm
pkgver=2.4.74
pkgrel=1
pkgdesc="Userspace interface to kernel DRM services"
arch=(i686 x86_64)
license=('custom')
depends=('libpciaccess')
makedepends=('valgrind' 'xorg-util-macros' 'libxslt' 'docbook-xsl')
checkdepends=('cairo')
replaces=('libdrm-new' 'libdrm-nouveau')
url="http://dri.freedesktop.org/"
source=(https://dri.freedesktop.org/$pkgname/$pkgname-$pkgver.tar.bz2{,.sig}
        COPYING)
sha256sums=('d80dd5a76c401f4c8756dcccd999c63d7e0a3bad258d96a829055cfd86ef840b'
            'SKIP'
            '9631d4f694952e3e6ae5a05534c2e93e994e47d3413677a3a00e45c8cef6db93')
validpgpkeys=('B97BD6A80CAC4981091AE547FE558C72A67013C3') # Maarten Lankhorst <maarten.lankhorst@canonical.com>
validpgpkeys+=('215DEE688925CCB965BE5DA97C03D7797B6E1AE2') # Damien Lespiau <damien.lespiau@intel.com>
validpgpkeys+=('10A6D91DA1B05BD29F6DEBAC0C74F35979C486BE') # David Airlie <airlied@redhat.com>
validpgpkeys+=('8703B6700E7EE06D7A39B8D6EDAE37B02CEB490D') # Emil Velikov <emil.l.velikov@gmail.com>
validpgpkeys+=('D6285B5E899299F3DA746184191C9B905522B045') # Rob Clark <robclark@freedesktop.org>
validpgpkeys+=('E8EB5B34081CE1EEA26EFE195B5BDA071D49CC38') # Kenneth Graunke <kenneth.w.graunke@intel.com>
validpgpkeys+=('FC9BAE1435A9F7F664B82057B5D62936D1FC9EE8') # Eric Anholt <eric@anholt.net>
validpgpkeys+=('3BB639E56F861FA2E86505690FDD682D974CA72A') # Matt Turner <mattst88@gmail.com>
validpgpkeys+=('C20F5C4490D7D64B4C9A09998CD1DF552975297B') # Robert Bragg <robert@sixbynine.org>

prepare() {
  cd $pkgname-$pkgver
  
  # pthread is useless in Linux
  sed -i "/pthread-stubs/d" configure.ac
  autoreconf --force --install

}
build() {
  cd $pkgname-$pkgver
  ./configure --prefix=/usr --enable-udev
  make
}

check() {
  cd $pkgname-$pkgver
  make -k check
}

package() {
  cd $pkgname-$pkgver
  make DESTDIR="$pkgdir" install
  install -m755 -d "$pkgdir/usr/share/licenses/$pkgname"
  install -m644 ../COPYING "$pkgdir/usr/share/licenses/$pkgname/"
}
