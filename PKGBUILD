# Maintainer: Caspar Friedrich <c.s.w.friedrich@gmail.com>

pkgname='python-esptool'
_name="esptool"
pkgdesc="A serial utility to communicate & flash code to Espressif ESP8266 & ESP32 chips"
pkgver=3.0
pkgrel=1
arch=('any')
url='https://pypi.org/project/esptool/'
license=('GPLv2+')
depends=('python-cryptography'
         'python-ecdsa'
         'python-pyaes'
         'python-pyserial')
makedepends=('python-setuptools')
source=("https://files.pythonhosted.org/packages/source/${_name::1}/${_name}/${_name}-${pkgver}.tar.gz")

build() {
    cd $srcdir/$_name-$pkgver
    python setup.py build
}

package() {
    cd $srcdir/$_name-$pkgver
    python setup.py install --root="$pkgdir" --optimize=1
}

sha256sums=('87953d235fed2c9adb1292b3769df0149686c9afdb1896dd963f730453cbc934')
