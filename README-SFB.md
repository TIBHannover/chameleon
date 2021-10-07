# Skin Customization for SFB1153 and SFB1368

There are different customizations for each of the mediawiki instances 

## Documentation
1. Install Chameleon Skin with customization (required)
2. Modify Customization (not required)

## 1. Install Chameleon Skin with customization (required)
* install the [Bootstrap](https://www.mediawiki.org/wiki/Extension:Bootstrap) extension and enable it in the LocalSettings.php
`wfLoadExtension( 'Bootstrap' );`
* clone the [Chameleon Repository](https://github.com/TIBHannover/chameleon) to the /skins directory, checkout the needed branch (sfb1153 or sfb1368) and enable the skin in the LocalSettings.php<br/>
`wfLoadSkin( 'chameleon' )`
* enable general layout customization in LocalSettings.php
`$egChameleonLayoutFile = __DIR__ . '/skins/chameleon/layouts/custom.xml;`
* enable style customization in LocalSettings.php
`$egChameleonExternalStyleModule =  __DIR__ . '/skins/chameleon/resources/styles/custom.scss';`

## 2. Modify Customization (not required)
* Disable cache in LocalSettings.php for development
`$egScssCacheType = CACHE_NONE;`
* modify the custom files (XML/SCSS)
