# Maintainer: Knut Ahlers <knut at ahlers dot me>

pkgname=gofumpt
pkgver=0.6.0
pkgrel=1
pkgdesc="A stricter gofmt"
arch=('i686' 'x86_64')
url="https://github.com/mvdan/gofumpt"
license=('custom')
makedepends=('go')
source=("${pkgname}-${pkgver}.tar.gz::https://github.com/mvdan/gofumpt/archive/v${pkgver}.tar.gz")
sha512sums=('6f7d6c769030ea499892b682f387e5c6875db6a9af7ee98f6af589ef83e508486e2f7807b805d13f8160a25eae440a930142f905d5c212b2bb5217eb0731a8f9')

build() {
	cd "${srcdir}/${pkgname}-${pkgver}"
	GO111MODULE=on go build -mod=readonly
}

package() {
	cd "${srcdir}/${pkgname}-${pkgver}"
	install -Dm755 -t "${pkgdir}/usr/bin" gofumpt
	install -Dm644 -t "${pkgdir}/usr/share/licenses/${pkgname}" LICENSE LICENSE.google
}
