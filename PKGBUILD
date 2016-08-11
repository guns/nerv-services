# Maintainer: guns <self@sungpae.com>
pkgname=nerv-services
pkgver=0
pkgrel=1
pkgdesc="Common system services"
arch=('any')
url="https://github.com/guns/nerv-services"
license=('MIT')
groups=('nerv')
backup=('etc/conf.d/chmod-backlight-control'
        'etc/conf.d/restrict-sysrq'
        'etc/conf.d/slock'
        'etc/usertmpfiles.yml')
depends=('iproute2'  # For `ip` to add 127.0.0.53
         'procps-ng' # For `pkill`
         'ruby'      # For `usertmpfiles`
         )
optdepends=('slock-nerv: For screen lock support'
            'sudo: For `slock` as a configurable user'
            'powertop: For powertop --auto-tune service')

pkgver() {
	printf %s.%s "$(git rev-parse --abbrev-ref HEAD)" "$(git rev-list HEAD --count)"
}

package() {
	cd "$startdir"
	rm -rf "$pkgdir"
	mkdir -p "$pkgdir"
	cp -R etc usr "$pkgdir"
}

# vim:noet:ts=8:sts=8:sw=8
