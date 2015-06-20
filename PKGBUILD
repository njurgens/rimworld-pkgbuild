# Author: Nick Jurgens <nicholas2010081@gmail.com>

pkgname='rimworld'
pkgver='0.11.834'
pkgrel='0'
pkgdesc='A sci fi colony sim driven by an intelligent AI storyteller.'
arch=('i686' 'x86_64')
url='http://rimworldgame.com/'
license=('custom')
source=('RimWorldAlpha11Linux.zip')
sha256sums=('eba6551f2c47a3927bdd09b861aacab4e0a0e0844360342b54d44c26ff1c5193')

package() {
	local _bin=/opt/rimworld/RimWorld834Linux.x86
	local _bindir=${pkgdir}/usr/local/bin
	local _installdir=${pkgdir}/opt/rimworld

	msg2 "Copying files into place"

	install -d -m 755 ${_installdir}
	cp -r ${srcdir}/RimWorld834Linux/. ${_installdir}

	msg2 "Creating link to executable"

	if [ $CARCH == 'x86_64' ]; then
		_bin=${_bin}_64
	fi

	install -d -m 755 ${_bindir}
	ln -s ${_bin} ${_bindir}/rimworld
	chmod +x ${pkgdir}/${_bin}
}
