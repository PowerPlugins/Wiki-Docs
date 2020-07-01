[DecimalFormat]: https://docs.oracle.com/javase/7/docs/api/java/text/DecimalFormat.html

# Options
The formatter expansion comes with two options that can be used in the `number_format` placeholders.

## `locale:<locale>`
Changes the used locale for the format. Depending on what locale is used does the resulting format look different.  
For example would `de:CH` display `1234` as `1'234` while `en:US` displays it as `1,234`.

This defaults to `en:US`  
Check the [locales](../locales) page for all available codes.

## `format:<format>`
This option allows you to set the format used in the placeholder.  
Please check the [Javadoc about DecimalFormat][DecimalFormat] for more information.
