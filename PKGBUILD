# Generated by gem2arch (https://github.com/anatol/gem2arch)
# Maintainer: Babken Vardanyan <483ken@gmail.com>

_gemname=diff-lcs
pkgname=ruby1.9-$_gemname
pkgver=1.2.5
pkgrel=1
pkgdesc='Diff::LCS computes the difference between two Enumerable sequences using the McIlroy-Hunt longest common subsequence (LCS) algorithm'
arch=(any)
url='http://diff-lcs.rubyforge.org/'
license=(MIT 'Perl Artistic v2' 'GNU GPL v2')
depends=(ruby1.9)
options=(!emptydirs)
source=(https://rubygems.org/downloads/$_gemname-$pkgver.gem)
noextract=($_gemname-$pkgver.gem)
sha1sums=('5f71a45f13780701f3a42297adc0269d0799e1d5')

package() {
  local _gemdir="$(ruby-1.9 -e'puts Gem.default_dir')"
  gem-1.9 install --ignore-dependencies --no-user-install -i "$pkgdir/$_gemdir" $_gemname-$pkgver.gem
  rm "$pkgdir/$_gemdir/cache/$_gemname-$pkgver.gem"
  install -D -m644 "$pkgdir/$_gemdir/gems/$_gemname-$pkgver/License.rdoc" "$pkgdir/usr/share/licenses/$pkgname/License.rdoc"
}
