# Maintainer:  Taras Shpot <mrshpot at gmail dot com>

pkgname=cl-salza2
_clname=salza2
pkgver=2.0.8
pkgrel=1
pkgdesc="a Common Lisp library for creating compressed data in the ZLIB, DEFLATE, or GZIP data formats"
arch=('i686' 'x86_64')
url="http://www.xach.com/lisp/salza2/"
license=('BSD')

depends=('common-lisp' 'cl-asdf')

install=cl-salza2.install
source=('http://www.xach.com/lisp/salza2.tgz')
md5sums=('ea20649a261fa0a7cd7ba45a547572ec')

build() {
  ### TODO: finish this. I've only filled in the versions ans URLs
    install -d ${pkgdir}/usr/share/common-lisp/source/${_clname}
    install -d ${pkgdir}/usr/share/common-lisp/systems
	install -d ${pkgdir}/usr/share/doc/${pkgname}

    cd ${srcdir}/${_clname}-${pkgver}

	install -m 644 -t ${pkgdir}/usr/share/common-lisp/source/${_clname} \
	  ${srcdir}/${_clname}-${pkgver}/*.lisp
	install -m 644 -t ${pkgdir}/usr/share/common-lisp/source/${_clname} \
	  ${srcdir}/${_clname}-${pkgver}/${_clname}.asd

	install -m 644 -t ${pkgdir}/usr/share/doc/${pkgname} \
	  ${srcdir}/${_clname}-${pkgver}/doc/*

	
    cd ${pkgdir}/usr/share/common-lisp/systems
    ln -s ../source/${_clname}/${_clname}.asd .
}

# vim:set ts=2 sw=4 et nospell:
