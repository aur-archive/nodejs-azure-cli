# Maintainer: Philipp Wolfer <ph.wolfer@gmail.com>

 _npmname=azure-cli
_npmver=0.8.10
pkgname=nodejs-${_npmname} # All lowercase
pkgver=${_npmver}
pkgrel=1
pkgdesc="Windows Azure Cross Platform Command Line tool"
arch=(any)
url="https://github.com/WindowsAzure/azure-sdk-tools-xplat"
license=(Apache)
depends=('nodejs')
optdepends=()
source=(http://registry.npmjs.org/$_npmname/-/$_npmname-$_npmver.tgz)
noextract=($_npmname-$_npmver.tgz)
options=(!strip)
sha1sums=('3c3f49607dbaa45789bd8df7b60596d7d9ae981f')

package() {
  cd $srcdir
  local _npmdir="$pkgdir/usr/lib/node_modules/"
  mkdir -p $_npmdir
  cd $_npmdir
  npm install -g --prefix "$pkgdir/usr" $_npmname@$_npmver
}

# vim:set ts=2 sw=2 et:
