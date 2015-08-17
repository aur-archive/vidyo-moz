pkgname=vidyo-moz
pkgver=3.0.4.001
pkgrel=2
pkgdesc="Desktop client for vidyo conferencing system used at Mozilla"
url="https://v.mozilla.org"
license=(commercial)
arch=(i686 x86_64)
makedepends=(rpmextract)
depends=(alsa-lib qt4 libidn glu dialog)
optdepends=('zenity: Perform checks at start'
'flashplugin: Join meetings via web browser')

if [ "$CARCH" = "i686" ]; then
rpmfilename="VidyoDesktopInstaller-sl5-TAG_VD_3_0_4_001.rpm"
md5sums=('b45fd0e221bd58c1731485dd51527a38')
elif [ "$CARCH" = "x86_64" ]; then
rpmfilename="VidyoDesktopInstaller-sl564-TAG_VD_3_0_4_001.rpm"
md5sums=('b0569d664e75c87056a75add207f0528')
fi

source=("https://v.mozilla.com/upload/${rpmfilename}")

package() {
cd $pkgdir
rpmextract.sh $srcdir/${rpmfilename}
}
