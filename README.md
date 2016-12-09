# Command line tools for tiling georeferenced raster data

## Table of Contents
  * [Download binary](#download-binary)
  * [Using ImageTiling](#using-imagetiling)
  * [Using CopyTiles](#using-copytiles)
  * [Building from Source](#building-from-source)
  
## Download Binary
[Download win-x64 binary](http://kosmosnimki.ru/downloads/tilingtools-101-win-x64.zip) ready for use package compiled with Microsoft Visual C++ 2013.

## Using ImageTiling

### Parameters
* **-i** - input raster file or file name template (**obligatory parameter**)
* **-ap** - flag parameter which turns off mosaic mode - each input file is processed apart. By default: one layer of tiles is generated (mosaic mode)
* **-o** - output file or folder. Default: output path is generated from input file(s) path
* **-z** - max zoom (base zoom). Default: max zoom is calculated from input raster file resolution and spatial reference system
* **-b** - vector clip mask. Default: is not defined
* **-minz** - min zoom. Default: 0 or 1
* **-tt** - tile type: png, jpg, jp2, tif. Default: jpg
* **-r** - resampling method tha is used to generate base zoom tiles (pyramid level tiles are generated from previous layer tiles by average resampling). Possible values: near, bilinear, cubic, lanczos. Default: cubic for general cases and near for rasters with index color table
* **-q** - compression quality 1-100. Default: 85
* **-of** - output tile container format: gmxtiles, mbtiles. Default: separate tiles 
* **-co** - creation options specific to output tile container format
* **-tsrs** - tiling spatial reference system. Possible values: 0 (World Mercator, EPSG:3395), 1 (Web Mercator or Spherical Mercatorv, EPSG:3857). Default value: 1 
* **-tnt** - output tile name templete. Default value: {z}/{x}/{y}
* **-nd** - nodata value. Default: isn't defined
* **-ndt** - nodata value tolerance. Default: isn't defined
* **-bgc** - background color. Default: black color - 0,0,0
* **-bnd** - raster band list order. Default: isn't defined
* **-wt** - working threads number. Default: 2
* **-pseudo_png** - code uint16 value into png red and green bands. Default: isn't defined
### Example


## Using CopyTiles



## Building from Source
Набор утилит для работы с тайлами.
Документация на сайте GeoMixer: http://geomixer.ru/index.php/ru/docs/manual/tilingtools.

Инструкция по компиляции:
- скопировать репозиторий
- разархивировать gdal210.zip в корень TilingTools в папку gdal210 
- открыть в VS2010 файл-проекта TilingTools.sln
- скомпилировать в конфигурации Release-x64 или Debug-x64
