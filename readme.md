# Codestar Framework
A Lightweight and easy-to-use WordPress Options Framework. It is a free framework for building theme options. Save your time!

## [Documentation](https://codestar.vercel.app)
Read the documentation for details [documentation](https://codestar.vercel.app)

## Installation
##### A) Usage as Theme
* Download zip file from github repository
* Extract download zip on `themename/cs-framework` folder under your theme directory
* Add framework include code on your theme `themename/functions.php` file

```php
require_once dirname( __FILE__ ) .'/cs-framework/cs-framework.php';
// -(or)-
require_once get_template_directory() .'/cs-framework/cs-framework.php';
```

* Yay! Right now you are ready to configure framework, metaboxes, taxonomies, wp customize, shortcoder
* Take a look for config files from `themename/cs-framework/config` folder
* Read for more from [documentation](https://codestar.vercel.app)

##### B) Usage as Plugin
* Download zip file from github repository
* **Way1** Extract download zip on `wp-content/plugins/cs-framework` folder under your plugin directory
* **Way2** Upload zip file from `wordpess plugins panel -> add new -> upload plugin`
* Active Codestar Framework plugin from wordpress plugins panel
* Yay! Right now you are ready to configure framework, metaboxes, taxonomies, wp customize, shortcoder
* Take a look for config files from `wp-content/plugins/cs-framework/config` folder also you can manage config files from theme directory. see overriding files method.
* Read for more from [documentation](https://codestar.vercel.app)

## Enable - Disable Mods
Add define code on your `themename/functions.php` directly.
```php
define( 'CS_ACTIVE_FRAMEWORK',   true  ); // default true
define( 'CS_ACTIVE_METABOX',     false ); // default true
define( 'CS_ACTIVE_TAXONOMY',    false ); // default true
define( 'CS_ACTIVE_SHORTCODE',   false ); // default true
define( 'CS_ACTIVE_CUSTOMIZE',   false ); // default true
```
or take a look for change define base code from `/cs-framework/cs-framework.php` directly.

## Enable Light Theme
Add the following define code somewhere in your theme or plugin, and light theme will be active.

```php
define( 'CS_ACTIVE_LIGHT_THEME',  true  ); // default false
```

## Overriding Files
You can override an existing file without change `themename/cs-framework` folder. just create one `themename/cs-framework-override` folder on your theme directory. for eg:

```php
themename/cs-framework-override/config/framework.config.php
themename/cs-framework-override/functions/constants.php
themename/cs-framework-override/fields/text/text.php
```

## Features
- Options Framework
- Metabox Framework
- Taxonomy Framework
- WP Customize Framework
- Shortcode Generator
- Supports Child Themes
- Validate Fields
- Sanitize Fields
- Localization
- Fields Dependencies
- Supports Multilangual Fields
- Reset/Restore/Export/Import Options
- and so much more...

## Options Fields
- Text
- Textarea
- Checkbox
- Radio
- Select
- Number
- Icons
- Group
- Image
- Upload
- Gallery
- Sorter
- Wysiwyg
- Switcher
- Background
- Color Picker
- Multi Checkbox
- Checkbox Image Select
- Radio Image Select
- Typography
- Backup
- Heading
- Sub Heading
- Fieldset
- Notice
- and **extendable** fields

## License
Codestar Framework is **free** to use both personal and commercial. If you used commercial, **please credit**.
Read more about GNU [license.txt](http://www.gnu.org/licenses/gpl-2.0.txt)

## The Latest Updates
#### 1.0.2
- Added: Support for WP Nav Menus select
- Added: Taxonomy framework clear form elements after saving
- Added: A filter for external icon-jsons load
- Added: An action `cs_customize_options_config` for customize config options
- Added: Auto Class name for all fields and generating classname by field title
- Added: Chinese language po/mo
- Added: Post type list support
- Added: Typenow param for specific metabox options
- Added: Light theme for framework
- Changed: Action from `cs_validate_save` to `cs_validate_save_after` for save after framework options
- Fixed: Color picker appears twice in widgets
- Fixed: Clear button of color-picker in customizer
- Fixed: Fieldset default value option
- Fixed: Overwrite issue for wp core get_locate() function
- Fixed: Call undefined function wp_get_current_user() issue
- Fixed: Minor bugs
- Updated: Chosen jquery plugin v1.6.1
- Updated: Google Fonts json for Typography field
- Updated: Font Awesome 4.7.0 icons package
- Updated: textdomain updates from __() to esc_html_e() - esc_html__()
- Updated: Backup field idea, changed from base64 encode/decode to seraize/unserialize
- Improved: Icons select field for avoid conflict
- Improved: Locate path function for windows servers
- Improved: Languages packages
- Removed: call_user_function idea
- Removed: custom/callback function support for field options

See [changelog](CHANGELOG.md)