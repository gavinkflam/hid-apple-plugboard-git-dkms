# Maintainer: Gavin Lam <me@gavin.hk>

pkgname='hid-apple-plugboard-git-dkms'
_pkgname=hid-apple-plugboard

pkgver=4.20.0
_pkgver=4.20.0
pkgrel=1

pkgdesc='GNU/Linux kernel module for customizable Apple keyboards. Change fn and other keys. (DKMS)'
arch=('any')
url='https://github.com/gavinkflam/hid-apple-plugboard'
license=('GPL2')

depends=('dkms')
makedepends=('git')

source=("git+https://github.com/gavinkflam/${_pkgname}.git#tag=${_pkgver}"
        'hid-apple-plugboard.conf'
        'config.h')

sha256sums=('SKIP'
            '4b94f1f55febddad5ff60a8918487b883ceadd4e6c3fb280e98e4e235cd09663'
            'deecad2cdc8beb2159e679065005665fe6ac6934004ce2aa80b2938ba9540ef7')

package() {
  install -dm755 ${pkgdir}/usr/src/${_pkgname}-${_pkgver}/
  install -Dm644 ${_pkgname}/* ${pkgdir}/usr/src/${_pkgname}-${_pkgver}/
  install -Dm644 config.h ${pkgdir}/usr/src/${_pkgname}-${_pkgver}/config.h
  install -Dm644 hid-apple-plugboard.conf ${pkgdir}/etc/depmod.d/hid-apple-plugboard.conf
}
