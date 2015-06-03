pkgname=grub-btrfs
pkgrel=1
pkgdesc="grub-btrfs, add support for btrfs snapshots into grub menu"
arch=('x86_64')
url="https://github.com/Antynea/grub-btrfs"
license=('GPL3')
depends=('btrfs-progs' 'bash' 'grub-common')
backup=('etc/grub.d/41_snapshots-btrfs')
source=('git+https://github.com/Antynea/grub-btrfs.git')
sha512sums=('SKIP')

pkgver() {
	cd "${pkgname}"
	( set -o pipefail
	git describe --long 2>/dev/null | sed 's/\([^-]*-g\)/r\1/;s/-/./g' ||
	printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
	)
}
package() {
	install -Dm 755 "${srcdir}/${pkgname}/41_snapshots-btrfs" "${pkgdir}/etc/grub.d/41_snapshots-btrfs"
}
