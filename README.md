# Command-line utilities for tiling georeferenced raster data

## Table of Contents
  * [Download binary](#download-binary)
  * [Using ImageTiling](#using-imagetiling)
  * [Using CopyTiles](#using-copytiles)
  * [Building from Source](#building-from-source)
  
## Download Binary
Download Win64 binary package compiled with Microsoft Visual C++ 2010.

## Using ImageTiling

### Parameters
* **-i** - input path
* **-ap** - tiling input files apart
* **-o** - output path
* **-z** - max zoom
* **"-b** - vector clip mask
* **-minz** - min zoom
* **-tt** - tile type: png, jpg, jp2, tif
* **-r** - resampling method
* **-q** - compression quality
* **-of** - tile container format:
* **-co** - creation options specific to output tile container format
* **-tsrs** - tiling srs. Default value:
* **-tnt** - tile name templete.
* **-nd** - nodata value.
* **-ndt** - nodata value tolerance
* **-bgc** - background color
* **-bnd** - raster band list order
* **-wt** - working threads number. Default: 2
* **-pseudo_png** - code uint value into png red and green bands

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
