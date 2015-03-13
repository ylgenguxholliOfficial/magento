magento
=======

1. Clone this repository your virtual host document root.  Make sure the document root targets ```/public``` inside of the directory.
2. Create ```/public/var``` and give it public read/write permissions (777)
3. Import the default database ```/tools/magento.sql```.
4. Run the following query, replacing ```DOMAIN``` with your Magento domain: ```update core_config_data set value = 'http://DOMAIN/' where path like '%/base_url';```
5. Do ```cp /public/app/etc/local.xml.template /public/app/etc/local.xml```. Then, ```/public/app/etc/local.xml``` with your new database details.  Also change the encryption key, ```<key><![CDATA[3c5f9bf38ee5a74d6d72edebed6e7639]]></key>```, before you start adding any data to your installation.
