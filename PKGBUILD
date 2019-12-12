# Maintainer: Ista Zahn <istazahn[at]gmail[dot]com>

pkgbase=python-altair
_pyname=altair
pkgname=('python-altair')
depends=('python' 'python-entrypoints' 'python-jsonschema' 'python-numpy' 'python-pandas' 'python-six' 'python-toolz')
makedepends=('python-setuptools')
optdepends=('python-selenium: png and svg export support')
pkgver=4.0.0
pkgrel=1
pkgdesc="Declarative statistical visualization library for Python"
arch=('any')
url="https://altair-viz.github.io/"
license=('MIT')
source=("${_pyname}-${pkgver}.tar.gz::https://files.pythonhosted.org/packages/00/db/8bb228681b548eea1dbcabb7be42c69ecf32f5e05afdfb8763fa3a66ed7e/${_pyname}-${pkgver}.tar.gz")
sha256sums=('92dcd7b84c715f8e02bbdf37e36193a4af8138b5b064c05f237e6ed41573880a')

package() {
  cd "${srcdir}/${_pyname}-${pkgver}"
  python setup.py install -O1 --root="${pkgdir}"
  install -Dm 644 LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
  install -Dm 644 README.md "${pkgdir}/usr/share/doc/${pkgname}/README"
}
