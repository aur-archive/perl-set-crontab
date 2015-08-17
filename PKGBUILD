# Contributor: Link Dupont <link.dupont@gmail.com>
# Maintainer: Link Dupont <link.dupont@gmail.com>
# Generator  : CPANPLUS::Dist::Arch 1.06
pkgname='perl-set-crontab'
pkgver='1.03'
pkgrel='1'
pkgdesc="Expand crontab(5)-style integer lists"
arch=('any')
license=('PerlArtistic' 'GPL')
options=('!emptydirs')
depends=('perl')
url='http://search.cpan.org/dist/Set-Crontab'
source=('http://search.cpan.org/CPAN/authors/id/A/AM/AMS/Set-Crontab-1.03.tar.gz')
md5sums=('c900a24a789203f4beebf91f5752e984')

build() {
  PERL=/usr/bin/perl
  DIST_DIR="${srcdir}/Set-Crontab-1.03"
  export PERL_MM_USE_DEFAULT=1 PERL5LIB=""                 \
    PERL_AUTOINSTALL=--skipdeps                            \
    PERL_MM_OPT="INSTALLDIRS=vendor DESTDIR='$pkgdir'"     \
    PERL_MB_OPT="--installdirs vendor --destdir '$pkgdir'" \
    MODULEBUILDRC=/dev/null

  { cd "$DIST_DIR" &&
    $PERL Makefile.PL &&
    make &&
    make test &&
    make install;
  } || return 1;

  find "$pkgdir" -name .packlist -o -name perllocal.pod -delete
}
