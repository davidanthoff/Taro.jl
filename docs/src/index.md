# Taro -- Work with Excel, Word and PDF files in Julia

Taro is a utility belt of functions to work with document files in Julia. It uses [Apache Tika](http://tika.apache.org/), [Apache POI](http://poi.apache.org) and [Apache FOP](https://xmlgraphics.apache.org/fop/)  (via [JavaCall](http://aviks.github.io/JavaCall.jl/)) to work with Word, Excel and PDF files.

##Package Features

 * Extract raw text from Word, Excel, PDF files
 * Extract tabular data from Excel files into a DataFrame (`readxl`, like `readtable`)
 * API to read and write Excel files from Julia
 * Convert `xsl-fo` files to PDFs for automated report generation

##Installation

```
julia> Pkg.add("Taro")
```

On installation, the `tika-app-1.4.jar` file will be downloaded from *Maven Central*
and `fop-2.0` will be downloaded from an Apache mirror.

##Usage

Before calling any function within this package, the `init()` method *must* be called.
This will set up the correct classpath, and initialise the JVM.

```@example
 using Taro
 Taro.init()
```
