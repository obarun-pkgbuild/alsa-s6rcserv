# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=alsa-s6rcserv
pkgver=0.1
pkgrel=1
pkgdesc="alsa service for s6"
arch=(x86_64)
license=('beerware')
depends=('alsa-utils' 's6' 's6-rc' 's6-boot')
conflicts=()
install=alsa-s6rcserv.install
source=('alsa.log.consumer-for'
		'alsa.log.run'
		'alsa.log.type'
		'alsa.logd'
		
		'alsa.longrun.finish'
		'alsa.longrun.pipeline-name'
		'alsa.longrun.producer-for'
		'alsa.longrun.run'
		'alsa.longrun.type'
		
		'alsa.oneshot.dependencies'
		'alsa.oneshot.down'
		'alsa.oneshot.type'
		'alsa.oneshot.up'
				
		'bundle.alsa.contents'
		'bundle.alsa.type'
		'LICENSE')
md5sums=('d1856123a07ab07963fe74a55bad5a48'
         '8f6c409ee8618b85f72538cbf1b98cff'
         '42c13bdd7f61c06ac59c1aaca9c0f07a'
         '69a7f577703dd587e92e25880bab1a07'
         '2328750376d094db633d5daa80feb19c'
         'e3b9aed009fccf0478842711625517b2'
         '122481500c5cdacb4d549d095c7428d6'
         'fa2ab33c06e6e3f90bcf8ab928987077'
         '42c13bdd7f61c06ac59c1aaca9c0f07a'
         'd1856123a07ab07963fe74a55bad5a48'
         '98687deb3ebbd87a531eafe5ac8cd4ea'
         '85bceea1fb94d4166f24496dc40a35e6'
         '63fdc4948b9ca1d16a91be9189113d33'
         '25ae451bb7ba9995e8a0ed621e3065ba'
         '71abe97e2554d37f1d12c5bf4945297f'
         '191a37ae657aa17e37e75d0242865dba')
validpgpkeys=('6DD4217456569BA711566AC7F06E8FDE7B45DAAC') # Eric Vidal

package() {
	
	# bundle , trouble here user-alsa need a maj at alsa e.g user-Base
	install -Dm 0644 "$srcdir/bundle.alsa.contents" "$pkgdir/etc/s6-serv/available/rc/bundle-Alsa/contents"
	install -Dm 0644 "$srcdir/bundle.alsa.type" "$pkgdir/etc/s6-serv/available/rc/bundle-Alsa/type"
	
	# longrun
	install -Dm 0644 "$srcdir/alsa.longrun.finish" "$pkgdir/etc/s6-serv/available/rc/alsa-longrun/finish"
	install -Dm 0644 "$srcdir/alsa.longrun.pipeline-name" "$pkgdir/etc/s6-serv/available/rc/alsa-longrun/pipeline-name"
	install -Dm 0644 "$srcdir/alsa.longrun.producer-for" "$pkgdir/etc/s6-serv/available/rc/alsa-longrun/producer-for"
	install -Dm 0644 "$srcdir/alsa.longrun.run" "$pkgdir/etc/s6-serv/available/rc/alsa-longrun/run"
	install -Dm 0644 "$srcdir/alsa.longrun.type" "$pkgdir/etc/s6-serv/available/rc/alsa-longrun/type"
	
	# oneshot
	install -Dm 0644 "$srcdir/alsa.oneshot.dependencies" "$pkgdir/etc/s6-serv/available/rc/alsa-oneshot/dependencies"
	install -Dm 0644 "$srcdir/alsa.oneshot.down" "$pkgdir/etc/s6-serv/available/rc/alsa-oneshot/down"
	install -Dm 0644 "$srcdir/alsa.oneshot.type" "$pkgdir/etc/s6-serv/available/rc/alsa-oneshot/type"
	install -Dm 0644 "$srcdir/alsa.oneshot.up" "$pkgdir/etc/s6-serv/available/rc/alsa-oneshot/up"
	
	# log
	install -Dm 0644 "$srcdir/alsa.log.consumer-for" "$pkgdir/etc/s6-serv/available/rc/alsa-log/consumer-for"
	install -Dm 0644 "$srcdir/alsa.log.run" "$pkgdir/etc/s6-serv/available/rc/alsa-log/run"
	install -Dm 0644 "$srcdir/alsa.log.type" "$pkgdir/etc/s6-serv/available/rc/alsa-log/type"

	# hook
	install -Dm 0644 "$srcdir/alsa.logd" "$pkgdir/etc/s6-serv/log.d/alsa-rc"
	
	install -Dm 0644 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/alsa-s6rcserv/LICENSE"
}
