# Development

## Get the latest webp-convert
`composer update`

## Building
`composer build`

This should produce the following
saved to '../build/latest/webp-on-demand-1.inc'
saved to '../build/latest/webp-convert.inc'
saved to '../build/latest/webp-on-demand-2.inc'

Next, test the single file build (webp-convert.inc) like this:
`composer test-webp-convert-build`

And then test the two-file build (`webp-on-demand-1.inc` and `webp-on-demand-2.inc`) like this:
`composer test-wod-build`


However, note that *hose tests are very minimal*. And that is not good, as the "build.php" file needs to be modified if there are added new base classes in webp convert. But such a problem will not be discovered by the tests.

So, before committing the build, you must run the WebPConvert tests as well, but using the build files instead. How to set this up? Perhaps we can utilize that the webp-convert tests are in the vendor folder?
