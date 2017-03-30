
### RAID

- Esta es la configuracion para un servidor de RAID 0:

![RAID0](/DNS/Ubuntu_RAID0.png)

- Esta es la configuracion para un servidor de RAID 5:

![RAID5](/DNS/UbuntuRAID5.png)

En ambos casos seran validos para un servidor DNS como el que vamos a configurar.

### DNS

Lo primero sera tener una maquina virtual con el Ubuntu server (En nuestro caso
utilizaremos un total de 5).

Al instalar el sistema operativo tendremos que configurarlo como uno de los anteriores.

Una vez que este instalada la maquina debemos instalar el bind9:

apt-install bind9

Despues empezaremos a configurar por el:

/etc/bind/named.conf.local

![named.conf.local](/DNS/named.conf.local.png)

Despues accederemos al:

/etc/bind/named.conf.options

![Options](/DNS/named.conf.options.png)

/etc/bind/rd.sitioa.com

/etc/bind/rd.sitioab.net

/etc/bind/rd.sitioc.net

![Options](/DNS/rd.sitioa.com.png)

![Options](/DNS/rd.sitiob.net.png)

![Options](/DNS/rd.sitioc.net.png)

Acontinuacion procedemos a configurar la inversa:

![Options](/DNS/ri.192.168.6.png)

- Para confirmar que todo esta correcto debemos introducir los siguientes comandos:


### RAID

- Esta es la configuracion para un servidor de RAID 0:

![RAID0](/DNS/Ubuntu_RAID0.png)

- Esta es la configuracion para un servidor de RAID 5:

![RAID5](/DNS/UbuntuRAID5.png)

En ambos casos seran validos para un servidor DNS como el que vamos a configurar.

### DNS

Lo primero sera tener una maquina virtual con el Ubuntu server (En nuestro caso
utilizaremos un total de 5).

Al instalar el sistema operativo tendremos que configurarlo como uno de los anteriores.

Una vez que este instalada la maquina debemos instalar el bind9:

apt-install bind9

Despues empezaremos a configurar por el:

/etc/bind/named.conf.local

![named.conf.local](/DNS/named.conf.local.png)

Despues accederemos al:

/etc/bind/named.conf.options

![Options](/DNS/named.conf.options.png)

/etc/bind/rd.sitioa.com

/etc/bind/rd.sitioab.net

/etc/bind/rd.sitioc.net

![Options](/DNS/rd.sitioa.com.png)

![Options](/DNS/rd.sitiob.net.png)

![Options](/DNS/rd.sitioc.net.png)

Acontinuacion procedemos a configurar la inversa:

![Options](/DNS/ri.192.168.6.png)

- Para confirmar que todo esta correcto debemos introducir los siguientes comandos:

named-checkconf

named-checkzone dam1 rd.dam1.com

Añadir a /etc/resolv.conf nuestro dns

/etc/init.d/bind9 restart

