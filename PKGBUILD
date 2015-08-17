# Contributor: 7kry <kt[at]7kry.net>

_gitname=tweepy
pkgname=python-tweepy-git
pkgver=1.11.r415.g78aebf9
pkgrel=1
pkgdesc='A Python library for accessing the entire Twitter API (GIT version, for Python3) .'
url='https://github.com/tweepy/tweepy'
license='MIT'
arch=('any')
depends=('python' 'python-six' 'python-requests-oauthlib')
makedepends=('git' 'python-pip')
conflicts=('python-tweepy')
provides=('python-tweepy')
source=(git://github.com/tweepy/tweepy.git)
md5sums=('SKIP')


pkgver() {
  cd "$_gitname"
  git describe --long | sed -r 's/([^-]*-g)/r\1/;s/-/./g'
}

build() {
  cd $srcdir/$_gitname
  python setup.py build
}

package() {
  cd $srcdir/$_gitname
  python setup.py install --root=$pkgdir --prefix=/usr
}
