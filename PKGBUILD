# Maintainer: Noah Vogt (noahvogt) <noah@noahvogt.com>

# binary version of this package (-bin): github.com/noahvogt/chromium-extension-return-youtube-dislike-bin

_extension=return-youtube-dislike
_id=gebbhagfogifgggkldgodflihgfeippi
pkgname="chromium-extension-$_extension"
pkgver=3.0.0.14
pkgrel=3
pkgdesc="Return YouTube Dislike - chromium extension"
arch=('any')
depends=('chromium')
url="https://github.com/noahvogt/return-youtube-dislike"
license=('GPL3')
source=("https://github.com/noahvogt/$_extension/releases/download/v$pkgver-$pkgrel/$_extension-$pkgver.crx")
noextract=("$_extension-$pkgver.crx")
sha256sums=('54b6d67a7f14752720bd6432b53c85f7a4fcad246635217e59af1eb576ec95f2')

build() {
    echo "{ \"external_crx\": \"/usr/share/$pkgname/$pkgname.crx\", \"external_version\": \"$pkgver\" }" > "$_id".json
}

package() {
    install -Dm644 "$_extension-$pkgver.crx" "$pkgdir/usr/share/$pkgname/$pkgname.crx"
    install -Dm644 "$_id".json "$pkgdir/usr/share/chromium/extensions/$_id.json"
}
