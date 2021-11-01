# Skin Customization for SFB1153 and SFB1368

There are different customizations for each of the mediawiki instances 

## Documentation
1. Install Chameleon Skin with customization (required)
2. Modify Customization (not required)

## 0. Uninstall the upstream Chameleon skin (if installed)
As mentioned in [README.md](./README.md)
> Remove the Chameleon skin from the composer.local.json file. Then run composer update "mediawiki/chameleon-skin" from the MediaWiki installation directory.

## 1. Install Chameleon Skin with customization (required)
* install the [Bootstrap](https://www.mediawiki.org/wiki/Extension:Bootstrap) extension and enable it in the LocalSettings.php
`wfLoadExtension( 'Bootstrap' );`
* clone the [Chameleon Repository](https://github.com/TIBHannover/chameleon) to the /skins directory with branch:
  * [sfb1153](https://github.com/TIBHannover/chameleon/tree/sfb1153) `git clone https://github.com/TIBHannover/chameleon.git -b sfb1153`  
  * [sfb1368](https://github.com/TIBHannover/chameleon/tree/sfb1368) `git clone https://github.com/TIBHannover/chameleon.git -b sfb1368` 
* enable the skin in the LocalSettings.php<br/>
`wfLoadSkin( 'chameleon' )`
* enable general layout customization in LocalSettings.php
`$egChameleonLayoutFile = __DIR__ . '/skins/chameleon/layouts/custom.xml';`
* enable style customization in LocalSettings.php
`$egChameleonExternalStyleModules =  [ __DIR__ . '/skins/chameleon/resources/styles/custom.scss' ];`


## 2. Modify Customization (not required)
* Disable cache in LocalSettings.php for development
`$egScssCacheType = CACHE_NONE;`
* modify the custom files (XML/SCSS)
