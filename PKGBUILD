# $Id$
# Maintainer: Jan de Groot <jgc@archlinux.org>
# Maintainer: Clément Guérin <geecko.dev@free.fr>

pkgname=libdrm-amd
_pkgname=libdrm
pkgver=2.4.74
pkgrel=1
pkgdesc="Userspace interface to kernel DRM services with AMDGPU-PRO additions"
arch=(i686 x86_64)
license=('custom')
depends=('libpciaccess')
makedepends=('valgrind' 'xorg-util-macros' 'libxslt' 'docbook-xsl')
checkdepends=('cairo')
provides=('libdrm')
conflicts=('libdrm')
replaces=('libdrm-new' 'libdrm-nouveau')
url="http://dri.freedesktop.org/"
source=(https://dri.freedesktop.org/$_pkgname/$_pkgname-$pkgver.tar.bz2{,.sig}
        COPYING
        '0026-amdgpu-add-the-interface-of-waiting-multiple-fences.patch'
        '0027-amdgpu-tests-add-multi-fence-test-in-base-test.patch'
        '0028-amdgpu-add-query-for-aperture-va-range.patch'
        '0029-amdgpu-Implement-SVM-v2.patch'
        '0030-amdgpu-SVM-test-v2.patch'
        '0031-amdgpu-Implement-multiGPU-SVM-support-v2.patch'
        '0032-tests-amdgpu-Add-test-for-multi-GPUs-SVM-test-v3.patch'
        '0033-tests-amdgpu-Add-verbose-outputs-v2.patch'
        '0034-amdgpu-Free-uninit-vamgr_32-in-theoretically-correct.patch'
        '0035-amdgpu-vamgr_32-can-be-a-struct-instead-of-a-pointer.patch'
        '0036-amdgpu-vamgr-can-be-a-struct-instead-of-a-pointer.patch'
        '0037-tests-amdgpu-add-the-heap-info-for-query.patch'
        '0038-amdgpu-reserve-SVM-range-explicitly-by-clients-v3.patch'
        '0039-amdgpu-expose-the-AMDGPU_GEM_CREATE_NO_EVICT-flag.patch'
        '0040-amdgpu-add-query-amdgpu-capability-defination.patch'
        '0041-amdgpu-add-query-amdgpu-pinning-memory-capability-de.patch'
        '0042-amdgpu-add-amdgpu_query_capability-interface.patch'
        '0043-amdgpu-add-amdgpu_find_bo_by_cpu_mapping-interface.patch'
        '0044-amdgpu-support-alloc-va-from-range.patch'
        '0045-tests-amdgpu-add-alloc-va-from-range-test.patch'
        '0047-tests-amdgpu-move-va_range_test-above-svm_test.patch'
        '0049-tests-amdgpu-remove-none-amdgpu-devices-for-hybrid-G.patch'
        '0056-amdgpu-change-max-allocation.patch'
        '0057-amdgpu-fix-print-format-error-V2.patch'
        '0061-amdgpu-add-bo-handle-to-hash-table-when-cpu-mapping.patch'
        '0062-amdgpu-cs_wait_fences-now-can-return-the-first-signa.patch'
        '0070-amdgpu-add-amdgpu_bo_inc_ref-function.patch'
        '0073-amdgpu-va-allocation-may-fall-to-the-range-outside-o.patch'
        '0074-drm-fix-a-bug-in-va-range-allocation.patch'
        '0077-amdgpu-Make-amdgpu_get_auth-to-non-static.patch'
        '0078-amdgpu-Add-interface-amdgpu_get_fb_id.patch'
        '0079-amdgpu-Add-interface-amdgpu_get_bo_from_fb_id.patch'
        '0080-amdgpu-tests-Add-the-test-case-for-amdgpu_get_fb_id-.patch'
        '0082-amdgpu-Fix-memory-leak-in-amdgpu_get_fb_id.patch'
        '0083-amdgpu-Fix-memory-leak-in-amdgpu_get_bo_from_fb_id.patch'
        '0104-drm-amdgpu-add-freesync-ioctl-defines.patch'
        '0108-amdgpu-tests-add-Polaris12-support-for-cs-test.patch'
        '0109-amdgpu-tests-remove-debug-info-in-cs-test.patch'
        '0114-amdgpu-add-more-capability-query.patch')
sha256sums=('d80dd5a76c401f4c8756dcccd999c63d7e0a3bad258d96a829055cfd86ef840b'
            'SKIP'
            '9631d4f694952e3e6ae5a05534c2e93e994e47d3413677a3a00e45c8cef6db93'
            '1252dd83009014f74cf92a9acb224124f68fda6250f071121bcb2f02984a82ba'
            'e89e8badcf65ae98f7f55281009ea672281c31be178ec816c81344fd86a7d85d'
            'c43566de52abdf9eccbc174a5cdc2e5abc2123231c9bd444d2b31e2e00092b1f'
            '02951ed298aeba7e61f5454f3cfe2d84289835464d349bd99acedf27903ae4b3'
            '9aa7db58255a7fe76f1245881a07ed5a7538d631e964fcd05bfbf091afd45fcb'
            'e40f620721f2998f327bf6c755416d8c102db878456d97d3e3ef532fef2e7e4c'
            'abbb994bf089a5f1758121f5223d42d2e60da134a74895edf62665dd5eadb62b'
            '2f3b274bf216f54aa70c15aa67edc887d5014ccddb0945731b83615d252404f1'
            '38781e984c09d181ff2f25086aff32d023ffe17d05db53e1277a35f0b1216045'
            '7ed86313809ee952d27ed1782d0e6886ff3e5ce22122be50b2448faedbea1be0'
            'b88e61c96e74dc3b2ea59c80a656e06646f8806c9f691f877df44a64b1573ead'
            'a35f1774ccb0182c240c1ac0c43ef5b81c1990bcb4bd61efaadf523b9dacb7d7'
            'e8cf606fece0fa00c19c7260de36675181255f2db9ee3cb3ce17fafe257dc82e'
            '3d2b052a7ec7ad98f81021aefc442b0a1d8387af85e969564500f8e297a955e6'
            'e216993f32bed5d030b61b10d05a2b23ad1e4bdb776ffcff45ade381ac28746d'
            'c4de12edd4efc5eb368fa0363c2be3d976ce99566d81457218194a5f7d0fa185'
            '29f509e8334a56b04fd2c8b10e8010238d6552e034354d0ba2d14a9f73a487aa'
            '359a4d1d37587f6dba987d2f31295119ece24a4f7dcf1ac678d445f2f6dc637d'
            'b0685f4982bb89f41ceb03a41e4dd1b1703d8fee7792e90aefb6ef75cc4b7d3c'
            'fb79fdea2d843ab4b2949c3f27210d43c63c620aee00a65a9f17bc546154f734'
            '51619672b227347c2dfc06494f3213b3d598c42aec6edc291648ba9083ae8f53'
            'c912ab270fdb79e5ac07516b844a3337d2cea29a49707a19113a5fd0d4b26d56'
            '3e66f2b34ccb8842ea75d98f95ab480d93b5dd1eb78dfe361053e9202012f3b5'
            '310830acf86337c52f3c396b56f347d97cf6108634231ced1f4ee91818843abb'
            'e0ef45f431b3904218f2313b43f89d4d7d6b1725335483f4548a0945724ac0f5'
            '78090b359aff9a572a563000b91e004e2805897e3efa351a75c06635805308ce'
            '26914b9341fc6d3b0d71cf3c56530c86395e8615ee6d5da8c57fcfaf2505cd7c'
            '83181b7c5bde73caee029c2603f1902856070d4c5d5a76a926ca67b76dadbc0a'
            '3511154c86db01db7b99ded9fec569d0f265293498cfa604614ae853d6b1e310'
            'ed7617f03d071e113319c2ea8717e3c66a880e09d70cfd3b7d075d0fbe684013'
            '4a6c6b175faca3d69ba00133e49eec3888ba07ab7c3da5f6f7ab8785f3c9c140'
            '579fb0e95c9a10b4cef8f2f8004316ad00186f310bc5f0c15e8f74a66dbd0955'
            '2623ad308faa3f9136c8011348de1db1fb9c089459c20d94be04e25ea3592674'
            '84af664b5f6c21e31622d38573569eeedbd0f1762ef908f77a28a4357b9342dc'
            'd01cad197875f29474bed3616ce88b9b29899935c1a4a0aba9b363259587f0ca'
            '3134fdb9568c5b83919543b64eaac6eb7fe2db43849f68f8046bf7adbde17dca'
            '19d0baa25d86692f3344cac16df9d0bacc3e2aaa552b21632a894c4b417b08d7'
            '77008fb2f8d6594c060036136d0c9afd4c78fbc7b77ebc5c8092d2e76de4d566'
            'fe2ccb157c87bcffe148bd30651bde68d997845c003cabd1408f3f358ed08c84')
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
  cd $_pkgname-$pkgver

  for i in $(ls ../*.patch)
  do
    patch -p1 -i $i
  done

  # pthread is useless in Linux
  sed -i "/pthread-stubs/d" configure.ac
  autoreconf --force --install

}
build() {
  cd $_pkgname-$pkgver
  ./configure --prefix=/usr --enable-udev
  make
}

check() {
  cd $_pkgname-$pkgver
  # make -k check
}

package() {
  cd $_pkgname-$pkgver
  make DESTDIR="$pkgdir" install
  install -m755 -d "$pkgdir/usr/share/licenses/$_pkgname"
  install -m644 ../COPYING "$pkgdir/usr/share/licenses/$_pkgname/"
}
