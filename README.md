Internet Positif
Menggunakan Bind9 respond policy zone (RPZ)

#Centos 
nano /etc/named.conf
#Debian
nano /etc/bind/named.conf.options

#
#[...]
options {
#...
response-policy { zone "pornografi"; zone "pengaduan"; zone "kajian"; zone "malware"; };
#...
#[...]


# tamahkan zone
#centos
nano /etc/named.conf
#debian
nnao /etc/bind/named.conf.local

#[...]
zone "pornografi" {
        type master;
        file "/home/positif/porno.zone";
        allow-query {none;};
        };
zone "pengaduan" {
        type master;
        file "/home/positif/pengaduan.zone";
        allow-query {none;};
        };
zone "kajian" {
        type master;
        file "/home/positif/kajian.zone";
        allow-query {none;};
        };
zone "malware" {
        type master;
        file "/home/positif/malware.zone";
        allow-query {none;};
        };
#[...]

