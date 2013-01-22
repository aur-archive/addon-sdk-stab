# Contributor: Johannes Dewender  < arch at JonnyJD dot net >

pkgname=addon-sdk-stab
_pkgname=addon-sdk
pkgver=1.13rc2
pkgrel=1
pkgdesc="addon-sdk/jetpack stabilisation release"
url="http://blog.mozilla.com/addons/"
arch=('any')
license=('MPL2')
depends=('python2')
optdepends=('firefox' 'firefox-nightly')
makedepends=()
conflicts=()
replaces=()
backup=()
source=("https://ftp.mozilla.org/pub/mozilla.org/labs/jetpack/addon-sdk-${pkgver}.tar.gz")
install='addon-sdk.install'
md5sums=('ba26b7f4da3692a0112de30ecaf6c738')

build() {
  cd "${srcdir}/${_pkgname}-${pkgver}"
  grep -Rl python . | xargs sed -ri 's/([^!]|^)python(\s|$)/\1python2\2/g'
}

package() {
  mkdir "${pkgdir}/opt"
  cp -r "${srcdir}/${_pkgname}-${pkgver}" "${pkgdir}/opt/${pkgname}"
}

# vim:set ts=2 sw=2 et:
