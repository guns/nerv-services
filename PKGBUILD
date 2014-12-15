# Maintainer: guns <self@sungpae.com>
pkgname=nerv-services
pkgver=master.1
pkgrel=1
pkgdesc="Common system services"
arch=('any')
url="https://github.com/guns/nerv-services"
license=('MIT')
groups=('nerv')
backup=('etc/conf.d/restrict-sysrq')
depends=('iproute2' 'procps-ng')

pkgver() {
    printf %s.%s "$(git rev-parse --abbrev-ref HEAD)" "$(git rev-list HEAD --count)"
}

package() {
	cd "$startdir"
	rm -rf "$pkgdir"
	mkdir -p "$pkgdir"
	cp -R etc usr "$pkgdir"
}
