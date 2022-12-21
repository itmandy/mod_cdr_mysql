mod_cdr_mysql
=============

FreeSWITCH Module CDR MYSQL

apt-get install libmysql++-dev

Just copy this folder in /usr/local/src/freeswitch/src/mod/event_handlers/

      make
      make install
      
Add it to autoloadconfig/modules.conf.

Edit the file cdr_mysql.conf with your DB settings.
Add the cdr_mysql.conf file to autoloadconfig folder. 

Restart FreeSWITCH

```sql
CREATE TABLE IF NOT EXISTS `cdr` (

`id` int(11) NOT NULL AUTO_INCREMENT,

`direction` varchar(16) DEFAULT NULL,

`call_id` varchar(255) DEFAULT NULL,

`local_ip_v4` varchar(32) CHARACTER SET latin1 DEFAULT NULL,

`caller_id_number` varchar(255) CHARACTER SET latin1 DEFAULT NULL,

`context` varchar(32) DEFAULT NULL,

`destination_number` varchar(255) CHARACTER SET latin1 DEFAULT NULL,

`route` varchar(255) DEFAULT NULL,

`route_ip` varchar(32) DEFAULT NULL,

`start_stamp` timestamp NULL DEFAULT NULL,

`answer_stamp` timestamp NULL DEFAULT NULL,

`end_stamp` timestamp NULL DEFAULT NULL,

`duration` int(11) DEFAULT NULL,

`billsec` int(11) DEFAULT NULL,

`hangup_cause` varchar(64) CHARACTER SET latin1 DEFAULT NULL,

`uuid` varchar(255) CHARACTER SET latin1 DEFAULT NULL,

`read_codec` varchar(64) CHARACTER SET latin1 DEFAULT NULL,

`write_codec` varchar(64) CHARACTER SET latin1 DEFAULT NULL,

PRIMARY KEY (`id`)

) ENGINE=MyISAM DEFAULT CHARSET=utf8 AUTO_INCREMENT=11 ;
```
