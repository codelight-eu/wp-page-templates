# PageTemplates
A simple class that allows registering WordPress Page templates from plugins.

## Installation
```
composer require codelight-eu/page-templates
```

## Usage

It's super simple. Run this somewhere in your WordPress plugin:

```php
<?php

    $pageTemplates = new Codelight\PageTemplates\PageTemplates();
    $pageTemplates->addTemplate(
        WP_PLUGIN_DIR . '/my-custom-plugin/templates/my-awesome-template.php',
        "My Awesome Template's Human-Readable Name"
    );
```

This adds the template to your WordPress site's Page edit interface.
The ``addTemplate()`` function takes two params:

```php

    /**
     * Add a new custom template.
     *
     * @param $file string Full path to the template file
     * @param $name string Human-readable template name
     */
    public function addTemplate($file, $name)
    {
        $this->templates[$file] = $name;
    }
```
## Credits
This library was adapted from http://www.wpexplorer.com/wordpress-page-templates-plugin/
