# Maintainer: Stefan Tatschner <stefan@sevenbyte.org>

pkgname=prezto-prompt-rumpelsepp
pkgver=r5.8cf4c6b
pkgrel=1
pkgdesc="My personal prezto theme"
arch=('any')
url='https://gist.github.com/rumpelsepp/02cdb5bd05fe6949b17b'
license=('MIT')
depends=('prezto-git')
source=("${pkgname}::git+https://gist.github.com/02cdb5bd05fe6949b17b.git#commit=8cf4c6b0a4949aba38af15528d06e5f358928c34")
md5sums=('SKIP')

pkgver() {
  cd "$srcdir/$pkgname"
  #git describe --long | sed -E 's/([^-]*-g)/r\1/;s/-/./g'
  printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package(){
  cd "$srcdir/$pkgname"
  mkdir -p ${pkgdir}/usr/lib/prezto/modules/prompt/functions/
  cp -ra "$srcdir/$pkgname"/prompt_rumpelsepp_setup ${pkgdir}/usr/lib/prezto/modules/prompt/functions/
}
