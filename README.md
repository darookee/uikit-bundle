# RUiKitBundle

Use UiKit-Forms in Symfony2

## Installation

First you need to add ```r/uikit-bundle``` to ```composer.json```:

```json
{
    "require": {
        "r/uikit-bundle": "dev-master"
    }
}
```

You also need to add ```RUiKitBundle``` to your ```AppKernel.php```

```php
// app/AppKernel.php
// ...
class AppKernel extends Kernel
{
    // ...
    public function registerBundles()
    {
        $bundles = array(
            // ...
            new R\UiKitBundle\RUiKitBundle(),
        );
        // ...
        return $bundles
    }
    // ...
}
```

After that you have to let twig know about the form template

```yaml
# ...
twig:
    # ...
    form:
        resources:
            - 'RUiKitBundle::uikit-form.html.twig'
# ...
```

You have to include the UiKit Stylesheets and JavaScripts for yourself.
Essentially you also just could download the uikit-form.html.twig and use it
witout installing this bundle, note that you have to chnage the date and time
widgets to not use the `localizeddateformat` function and supply you own format
for the uikit-date- and -timepicker.

The UiKit Components you need to include at least are these

- form-select
- form-password
- form-file
- form-advanced
- placeholder
- autocomplete
- datepicker
- timepicker
