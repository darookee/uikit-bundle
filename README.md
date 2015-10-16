# RUiKitBundle

Use UiKit in Symfony

## Dependencies

- bower
- Assetic with the less filter enabled

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

Additionally you have to enable the less filter in your Assetic configuration.

If composer did not run ```bower install``` after installing the bundle please
run it manually in the module path to install uikit.
