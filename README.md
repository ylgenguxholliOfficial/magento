magento
=======

1. Clone this repository your virtual host document root.  Make sure the document root targets ```/public``` inside of the directory.
2. Import the default database ```/tools/magento.sql```.
3. Run the following query, replacing ```DOMAIN``` with your Magento domain: ```update core_config_data set value = 'http://DOMAIN/' where path like '%/base_url';```
4. Update ```/public/app/etc/local.xml``` with your new database details.
