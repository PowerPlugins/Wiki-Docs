[DecimalFormat]: https://docs.oracle.com/javase/7/docs/api/java/text/DecimalFormat.html

# Options
In some cases do you want the `format` option to display the number in a different way, be it how the sections are divided or how large each section is.  
For that does the expansion offer the `%formatter_number_format_[locale]:[format]_<number>%` placeholder to override the default ones set in the config.yml of PlaceholderAPI.

## locale
Changes the used locale for the format. Depending on what locale is used does the resulting format look different.  
For example would `de-CH` display `1234` as `1'234` while `en-US` displays it as `1,234`.

This defaults to `en-US`  
Check the [locales](../locales) page for all available codes.

## format
This option allows you to set the format used in the placeholder.  
Please check the [Javadoc about DecimalFormat][DecimalFormat] for more detailed information on how the syntax looks like.
