# Maintainer: Knut Ahlers <knut at ahlers dot me>

pkgname=gofumpt
pkgver=0.5.0
pkgrel=1
pkgdesc="A stricter gofmt"
arch=('i686' 'x86_64')
url="https://github.com/mvdan/gofumpt"
license=('custom')
makedepends=('go')
source=("${pkgname}-${pkgver}.tar.gz::https://github.com/mvdan/gofumpt/archive/v${pkgver}.tar.gz")
sha512sums=('84e5dfbdc9c35b9b0eb9734951140ebf0d1d76e7a11753864997295b83451f1ac54247a697f3d8ceb4afe4e7c4c259392c82af78849df97ef1608bef52240e5f')

build() {
	cd "${srcdir}/${pkgname}-${pkgver}"
	GO111MODULE=on go build -mod=readonly
}

package() {
	cd "${srcdir}/${pkgname}-${pkgver}"
	install -Dm755 -t "${pkgdir}/usr/bin" gofumpt
	install -Dm644 -t "${pkgdir}/usr/share/licenses/${pkgname}" LICENSE LICENSE.google
}
