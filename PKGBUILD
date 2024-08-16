# Maintainer: Knut Ahlers <knut at ahlers dot me>

pkgname=gofumpt
pkgver=0.7.0
pkgrel=1
pkgdesc="A stricter gofmt"
arch=('i686' 'x86_64')
url="https://github.com/mvdan/gofumpt"
license=('custom')
makedepends=('go')
source=("${pkgname}-${pkgver}.tar.gz::https://github.com/mvdan/gofumpt/archive/v${pkgver}.tar.gz")
sha512sums=('98fd56046c6f93af1ecb4f488e476090836853b9de85dc092814778a58ddfd55655f5696c4b7b549274f3e21d6442d02ddaf2472f481f94183093002c3990130')

build() {
	cd "${srcdir}/${pkgname}-${pkgver}"
	GO111MODULE=on go build -mod=readonly
}

package() {
	cd "${srcdir}/${pkgname}-${pkgver}"
	install -Dm755 -t "${pkgdir}/usr/bin" gofumpt
	install -Dm644 -t "${pkgdir}/usr/share/licenses/${pkgname}" LICENSE LICENSE.google
}
