# webp-convert-concat
This project contains webp-convert concatenated to a single file as well as webp-convert concatenated to two files ([this case](https://github.com/rosell-dk/webp-convert/blob/master/docs/v2.0/webp-on-demand/without-composer.md)).

The idea behind these concats ("builds") is to make life easier for those old-school webmasters who manages their site with manual file transfers. In that case, dealing with a couple of large files is easier than dealing with a lot of small files.

The resulting builds are found in the `build` folder.

Note: If you are using *composer*, you do not need these builds.

This project also contains the scripts that creates these "builds" and tests.

All the files in this project used to be part of `webp-convert` but has been moved to this repo.


## The build files

`webp-convert.inc`:
An aggregation of all the php files needed, with base classes on top. It also includes the required library: rosell-dk/image-mime-type-guesser.

`webp-on-demand-1.inc`
(which only consists of a few classes)

`webp-on-demand-2.inc`
Loaded by webp-on-demand-2 when a conversion is needed. It contains the rest of the library.
