[DecimalFormat]: https://docs.oracle.com/javase/7/docs/api/java/text/DecimalFormat.html

This page lists all available options that can be used within the placeholder.  
Depending on what option is used are other options ignored.

## `format:(format)`
The `format:(format)` option allows you to define the actual formatting of the number.  
For example would `format:(#,###,###.##)` turn `1000000` into `1,000,000`.

The formatting used is based on the [DecimalFormat] from Java.  
Note that the result may look different, based on what [locale](../locales) you use.

## `locale:(locale)`
This option allows you to change the locale used for the formatting.  
Some formatting is based on the currently used locale. For example would `de_DE` change `1000000` to `1.000.000` and `en_US` change it to `1,000,000`.

Visit the [locales](../locales) page for a list of (known) supported locales.

## `time`
The `time` option will enable time-conversion for the number.  
In this mode are all other options - with exception of the [values option](#values-values) - changed into a duration.  
For example would `100` become `1m 40s`.

You can change specific aspects of this, like f.e. the letters used for the time or if it should have spaces between each one, in the config.yml of PlaceholderAPI.

## `value:(value)`
This is the only required option.  
The value option is used to provide the number which should be formatted.  
You can also use placeholders which return whole numbers, but you'll need to use curved brackets instead of the percent symbold (i.e. `%placeholder%` becomes `{placeholder}`).
