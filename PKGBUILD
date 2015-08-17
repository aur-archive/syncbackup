# Contributor: Artem A. Klevtsov <unikum.pm@gmail.com>

pkgname=syncbackup
pkgver=1.1.4
pkgrel=1
pkgdesc="Front-end of rsync for backup purposes writen on Qt"
arch=('i686' 'x86_64')
url='http://www.darhon.com/syncbackup'
license=('GPL3')
depends=('qt4' 'rsync')
optdepends=('openssh-askpass: support authentication by password'
	    'ksshaskpass: support authentication by password in KDE4')
install="${pkgname}.install"
source=("http://www.darhon.com/sites/default/files/downloads/apps/${pkgname}_${pkgver}.tar_.gz")
md5sums=('ef95af81574c55d96161adccc88f28e9')

build() {
  cd "${srcdir}/pkg"
  qmake-qt4
  make
}

package() {
  cd "${srcdir}/pkg"
  make INSTALL_ROOT=${pkgdir} install
}
