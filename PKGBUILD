# Generated by gem2arch (https://github.com/anatol/gem2arch)
# Maintainer: Anatol Pomozov <anatol.pomozov@gmail.com>
# Contributor: Alfredo Palhares <masterkorp@masterkorp.net>

_gemname=capistrano
pkgname=ruby-$_gemname
pkgver=3.4.0
pkgrel=1
pkgdesc='Capistrano - Welcome to easy deployment with Ruby over SSH'
arch=(any)
url='http://capistranorb.com/'
license=(MIT)
depends=(ruby ruby-sshkit ruby-capistrano-stats ruby-i18n)
options=(!emptydirs)
source=(https://rubygems.org/downloads/$_gemname-$pkgver.gem)
noextract=($_gemname-$pkgver.gem)
sha1sums=('a2935425e76fc40d395119b9ab8cb0cc420c7830')

package() {
  local _gemdir="$(ruby -e'puts Gem.default_dir')"
  gem install --ignore-dependencies --no-user-install -i "$pkgdir/$_gemdir" -n "$pkgdir/usr/bin" $_gemname-$pkgver.gem
  rm "$pkgdir/$_gemdir/cache/$_gemname-$pkgver.gem"
  install -D -m644 "$pkgdir/$_gemdir/gems/$_gemname-$pkgver/LICENSE.txt" "$pkgdir/usr/share/licenses/$pkgname/LICENSE.txt"
}
