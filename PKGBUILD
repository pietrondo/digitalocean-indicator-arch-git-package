# Maintainer: Pietro Capriata <pietro.capriata@gmail.com>

_pkgname='digitalocean-indicator'
pkgname=$_pkgname-git
pkgrel=1

pkgdesc='Manage Digital Ocean droplets from your desktop'
arch=('any')
url='https://github.com/andrewsomething/digitalocean-indicator'
license=('GPL')
depends=('python2' 'libappindicator-gtk3' 'python2-pip')
conflicts=('digital-ocean')
#install=$pkgname.install
md5sums=('SKIP')
source=('git://github.com/andrewsomething/digitalocean-indicator')

pkgver() {
    cd "$srcdir/$_pkgname"
    echo $(git rev-list --count master).$(git rev-parse --short master)
}

package() {
  cd $srcdir/$pkgname
	
	python2 setup.py install --prefix=/usr --root=${pkgdir}
}

# vim 
