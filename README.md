# RimWorld PKGBUILD


## Description

Use this `PKGBUILD` to build and install RimWorld alpha 11.  You need to have
your own copy of RimWorld.  If you don't already have a copy of RimWorld, you
can grab one here: http://rimworldgame.com/.


## Instructions

	# clone the repo
	git clone https://github.com/njurgens/rimworld-pkgbuild.git


	# copy the RimWorld zip file into the same directory as the `PKGBUILD`.
    cp /path/to/RimWorldAlpha11.zip rimworld-pkgbuild/


	# run makepkg to build and install
	cd rimworld-pkgbuild
	makepkg --install
