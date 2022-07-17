##  URN catalog

Magento code references all XSD schemas as Uniform Resource Names (URNs). If you’re developing code and need to reference XSDs, your integrated developer environment (IDE) to recognize and highlight URNs. This makes development easier.

``
<config xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:noNamespaceSchemaLocation="urn:magento:module:Magento_Store:etc/config.xsd">
``

Run these magento2 cli command 
  - bin/magento is the CLI of Magento2
  - .idea/misc.xml is the location where we tell PHPStorm the URNs structure.

``
bin/magento dev:urn-catalog:generate .idea/misc.xml
``
If you go to Preferences > Languages & Frameworks > Schemas and DTDs, you will see the urn:magento:framework configurations.

## Code Sniffer

PHP CodeSniffer (PHPCS) is a set of two PHP scripts; the main phpcs script that tokenizes PHP, JavaScript and CSS files to detect violations of a defined coding standard, and a second phpcbf script to automatically correct coding standard violations. PHP CodeSniffer is an essential development tool that ensures your code remains clean and consistent.

In PhpStorm, we can configure code style through Preferences > Editor > Inspections > PHP > Code Sniffer and use one of the many available schemes. In this case, we’ll use the one that Magento provides us, and it is in the following directory:

``
dev/tests/static/testsuite/Magento/Test/Php/_files/phpcs/
``
![screenshot](coesniffer.png)

![coesniffer.png](https://jokiruiz.com/wp-content/uploads/2017/05/phpcs_ok.png)
![https://jokiruiz.com/wp-content/uploads/2017/05/phpcs_ok.png](https://jokiruiz.com/wp-content/uploads/2017/05/phpcs_wrong.png)

## Mess Detector

PHPMD can be seen as an user friendly and easy to configure front-end for the raw metrics measured by PHP Depend. What PHPMD does is: It takes a given PHP source code base and look for several potential problems within that source. These problems can be things like Possible bugs, Sub-optimal code, Over-complicated expressions, Unused parameters, methods, properties etc.

In PhpStorm, we can configure code style through Preferences > Editor > Inspections > PHP > Mess Detector and use one of the many available schemes. In this case, we’ll use the one that Magento 2 provides us, and it is in the following directory:

``
dev/tests/static/testsuite/Magento/Test/Php/_files/phpmd/
``

![phpmd](https://jokiruiz.com/wp-content/uploads/2017/05/phpmd_phpstorm_mage2-1024x637.png)

Preferences > Languages & Frameworks > PHP > Mess Detector. Magento 2 provides a binary in the following directory:

``
vendor/bin/phpmd
``

## Exclude directories
