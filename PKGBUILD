# Maintainer: hiruocha <hiruocha[at]outlook[dot]com>
# Contributor: Super Tecno Gym <banana@grrlz.net>
# Contributor: Sam Day <me@samcday.com>

pkgname=rmtfs
pkgver=1.3
pkgrel=1
pkgdesc="Qualcomm Remote Filesystem Service Implementation"
arch=('aarch64')
url="https://github.com/linux-msm/rmtfs"
license=('BSD-3-Clause')
depends=('qrtr' 'libudev.so')

source=("$pkgname-$pkgver.tar.gz::$url/archive/refs/tags/v$pkgver.tar.gz")
sha256sums=('4b6c398806a1046e2256a685d592833de0f37b7245b8adc4797e1791f0e117ee')

build() {
  cd "$pkgname-$pkgver"
  make
}

package() {
  cd "$pkgname-$pkgver"
  make prefix=/usr DESTDIR="$pkgdir" install
  install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
