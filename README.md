# Welcome to Planet Suite pages

Planet is a suite of component modules developed with [py4web](http://py4web.com/) web framework and thought as useful tools for quick develop web applications designed around spatial or geographical data.

## The Suite

[Planetstore](https://github.com/manuelep/planetstore) | [Planetclient](https://github.com/manuelep/planetclient) | [iTile](https://github.com/manuelep/itile)
------------ | ------------- | -------------

## Notes

Before start reading forward let me tell you that even if I tried to think this suite as more general as possible I necessarily refered to some specific requirement such as:

* [PostGIS](https://postgis.net/)
    That nowaday is the most powerful free engine (actually a database engine extension) for managing spatial or geographic data.

# Components

## [Planetstore](https://github.com/manuelep/planetstore)

This module implements a database model inspired to the OpenstreetMap database optimized for storing informations with a very flexible structure based on **json** standard able to host any kind of data.

It supports OpenstreetMap and geojson as main data structure for import.

The high level geometric structures management of lines, polygons and other is done with some views or [named queries](https://www.postgresqltutorial.com/postgresql-views/) that give an easy interface for interacting with theese kind of complex gemetries.

This views structure is used for managing complex geometries even out of the OpenstreetMap concepts such as in the case of street graphs and space syntax analysis.

This module implements tools for easy serve and manage vector data using useful standard geometric structures such the [classic squares tiles](https://wiki.openstreetmap.org/wiki/Tiles) and [Uber hexagonal tiles](https://eng.uber.com/h3/) directly at the database level (PostGIS only).

## [Planetclient](https://github.com/manuelep/planetclient)

Requires: Planetstore

This module implements the database model using the *database abstractiuon layer* [PyDAL](https://github.com/web2py/pydal/) for easy IO web services implementation.

It implements tools for easy serve and manage vector data using the cited tile structures even at the python environment level.

## [iTile](https://github.com/manuelep/itile)

This module implements helpers base on the [Mapnik](https://mapnik.org/) python library for easy raster tile layer services implementation.
