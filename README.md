# O9coin.com

This O9Coin  runs on a linux environment with PHP and MYSQL, and it was tested on Ubuntu 15.04 with PHP 5.6.4 and MariaDB 5.5.


First of all you need to create a new database and create this table on it for the O9Coin  to save all requests:

CREATE TABLE IF NOT EXISTS `create_wallet` (
`id` bigint(20) unsigned NOT NULL,
  `ip_address` varchar(45) NOT NULL,
  `wallet_address` varchar(100) NOT NULL,
  `wallet_id` varchar(75) NOT NULL,
  `timestamp` datetime NOT NULL
) ENGINE=InnoDB AUTO_INCREMENT=1 DEFAULT CHARSET=latin1;
After you create database you need to edit config.php with all your custom parameters and also database information.

Now for O9Coin  to communicate with O9Coin wallet you need to run simplewallet.

wallet.bin needs to be the wallet file name that you enter when you created your wallet.
password needs to be the password to open your wallet
rpc-bind-port and rpc-bind-ip can be changed if so, you need to edit index.php and request.php (Please don't edit, as you may end opening the wallet rpc to the public)
And O9Coin daemon as this:

Advertisements can be edited on the index.php they are between this lines for an easy location:

After all this steps you should be ready to go ;)
