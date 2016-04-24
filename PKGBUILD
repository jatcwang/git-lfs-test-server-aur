# Maintainer: Michael Schubert <mschu.dev at gmail>
pkgname=git-lfs-test-server
pkgver=0.3.0
pkgrel=1
pkgdesc="An open source Git extension for versioning large files"
arch=('i686' 'x86_64')
url="https://git-lfs.github.com/"
license=('MIT')

_binname=lfs-test-server-linux

if [[ $CARCH == 'x86_64' ]]; then
  _arch=386
  _filename=Linux.$_arch
  md5sums=('202fdfa0c4b90b87865b8e3a75c7c1b9')
else
  _arch=amd64
  _filename=Linux.AMD64
  md5sums=('f6819014718743a1a53dc44db957575c')
fi

source=(https://github.com/github/lfs-test-server/releases/download/v$pkgver/$_filename.gz)

package() {
  cd "$srcdir"/$_binname-$_arch
  install -Dm755 lfs-test-server "$pkgdir"/usr/bin/lfs-test-server
}
