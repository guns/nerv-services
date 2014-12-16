# Maintainer: guns <self@sungpae.com>
pkgname=nerv-services
pkgver=
pkgrel=1
pkgdesc="Common system services"
arch=('any')
url="https://github.com/guns/nerv-services"
license=('MIT')
groups=('nerv')
backup=('etc/usertmpfiles.yml'
        'etc/conf.d/restrict-sysrq')
depends=('iproute2'     # For `ip`
         'procps-ng'    # For `pkill`
         'ruby'         # For `usertmpfiles`
         'slock-nerv'   # For `slock`
         'sudo'         # For `slock` as a configurable user
         )

pkgver() {
    printf %s.%s "$(git rev-parse --abbrev-ref HEAD)" "$(git rev-list HEAD --count)"
}

package() {
	cd "$startdir"
	rm -rf "$pkgdir"
	mkdir -p "$pkgdir"
	cp -R etc usr "$pkgdir"
}
