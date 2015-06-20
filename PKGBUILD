# Author: Nick Jurgens <nicholas2010081@gmail.com>

pkgname='rimworld'
pkgver='0.11.834'
pkgrel='1'
pkgdesc='A sci fi colony sim driven by an intelligent AI storyteller.'
arch=('i686' 'x86_64')
url='http://rimworldgame.com/'
license=('custom')
source=('RimWorldAlpha11Linux.zip')
sha256sums=('eba6551f2c47a3927bdd09b861aacab4e0a0e0844360342b54d44c26ff1c5193')

package() {
	msg2 "Copying files into place"

	local _installdir=${pkgdir}/opt/rimworld

	install -d ${_installdir}
	cp -r ${srcdir}/RimWorld834Linux/. ${_installdir}


	msg2 "Creating link to executable"

	local _bin=/opt/rimworld/RimWorld834Linux.x86
	local _bindir=${pkgdir}/usr/local/bin

	if [ $CARCH == 'x86_64' ]; then
		_bin=${_bin}_64
	fi

	install -d ${_bindir}
	ln -s ${_bin} ${_bindir}/rimworld
	chmod +x ${pkgdir}/${_bin}


	msg2 "Installing launcher and icon"

	local _icon=${srcdir}/RimWorld834Linux/RimWorld834Linux_Data/Resources/UnityPlayer.png
	local _icondir=${pkgdir}/usr/share/icons/hicolor/128x128/apps

	install -d ${_icondir}
	cp ${_icon} ${_icondir}/rimworld.png

	local _appdir=${pkgdir}/usr/share/applications

	install -d ${_appdir}
	cp ${startdir}/rimworld.desktop ${_appdir}
}
