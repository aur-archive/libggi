#Maintainer: Nathan O <ndowens04 at gmail dot com>
###16.04.2013###geany###Vladimir Zashelkin <aka-novaspirit@yandex.ru>

pkgname=libggi
pkgver=2.2.2
pkgrel=2
pkgdesc="GGI graphics library"
url="http://www.ggi-project.org/"
license=("MIT")
groups=('ggi')
depends=('aalib' 'libxxf86vm' 'libgii')
source=("http://downloads.sourceforge.net/ggi/$pkgname-$pkgver.src.tar.bz2" "LICENSE")
md5sums=('51d92ea810dad5360f6f0d02dd8b84a4' '76299c9337a881c385af535626deb928')
arch=('i686' 'x86_64')
options=('!libtool')

build() {
	
cd ${startdir}
  
  echo 
echo "Название программы ============> ${pkgname}"
sleep 0.4
echo "Версия программы ==============> ${pkgver}"
sleep 0.4
echo "Начальный каталог =============> ${startdir}"
sleep 0.4
echo "Каталог с исходным кодом ======> ${srcdir}"
sleep 0.4
echo "Каталог с собранным пакетом ===> ${pkgdir}"
sleep 0.4
echo ""



echo ""
echo "Пуск"
sleep 2

cd ${srcdir}/${pkgname}-${pkgver}

./configure --prefix=/usr --sysconfdir=/etc --mandir=/usr/share/man
make 
  
}


package() {
cd ${srcdir}/${pkgname}-${pkgver}

make DESTDIR=${pkgdir} install
mkdir -p ${pkgdir}/usr/share/licenses/${pkgname}
install -Dm644 ${srcdir}/LICENSE ${pkgdir}/usr/share/licenses/${pkgname}

}

