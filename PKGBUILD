pkgname=grub-btrfs
pkgrel=1
pkgver=1.7.2
pkgdesc="grub-btrfs, add support for btrfs snapshots into grub menu"
arch=('x86_64')
url="https://github.com/Antynea/grub-btrfs"
license=('GPL3')
depends=('btrfs-progs' 'bash' 'grub')
backup=('etc/grub.d/41_snapshots-btrfs')
source=('git+https://github.com/Antynea/grub-btrfs.git')
sha512sums=('SKIP')

package() {
	install -Dm 755 "${srcdir}/${pkgname}/41_snapshots-btrfs" "${pkgdir}/etc/grub.d/41_snapshots-btrfs"
}
