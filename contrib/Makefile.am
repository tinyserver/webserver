## Cherokee: Makefile.am  -*- makefile -*-

SUFFIXES = .pre

.pre:
	sed -e "s|%sysconfdir%|${sysconfdir}|g; s|%sbindir%|${sbindir}|g; s|%docdir%|${docdir}|g; s|%prefix%|${prefix}|g; s|%localstatedir%|${localstatedir}|g; s|%libdir%|${libdir}|g; s|%wwwroot%|${WWW_ROOT}|g; s|%version%|${PACKAGE_VERSION}|g; s|%phpcgi%|${PHPCGI}|g; s|%datadir%|${datadir}|g; s|%localedir%|${localedir}|g" $< > $@

EXTRA_DIST = \
cherokee.pre \
bin2buffer.py \
tracelor.py \
make-cert.sh \
make-dh_params.sh

CLEANFILES = \
cherokee \
server.pem \
rand.dat \
cakey.key \
cakey.csr \
cakey.pem

all-local: cherokee
