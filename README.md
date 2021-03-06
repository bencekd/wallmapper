# Wallmapper

A simple Python script that helps you create high resolution wallpapers from Mapbox maps.

Although Mapbox has a [static API](https://www.mapbox.com/developers/api/#Static.API),
it imposes a limit of 1280x1280 pixels.
This script downloads individual tiles and knit them together to reach bigger resolutions.
That way, you can use these beautiful maps as the wallpaper image of your favorite smartphone and/or tablet.

Note: Printing maps is not covered by the Mapbox TOS. If you'd like to print your maps, ask for permission first.

## Usage

Make sure you have a MapBox account, and you replace the `examples` tileset with a tileset in your Mapbox account.

Run the `--help` for an overview of the available options:

```
$ python wallmapper.py -h
usage: Wallmapper [-h] [--width WIDTH] [--height HEIGHT] [--latitude LATITUDE]
                  [--longitude LONGITUDE] [--zoom ZOOM] [--basemap BASEMAP]
                  [--output OUTPUT] [--stats STATS]

Create high resolution wallpapers from Mapbox maps.

optional arguments:
  -h, --help            show this help message and exit
  --width WIDTH         Wallpaper width (default: 2160)
  --height HEIGHT       Wallpaper height (default: 1920)
  --latitude LATITUDE   Latitude (default: 38.9101)
  --longitude LONGITUDE Longitude (default: -77.0485)
  --zoom ZOOM           Zoom level (default: 17)
  --basemap BASEMAP     Mapbox basemap (default: eleanor.mnyzxgvi)
  --output OUTPUT       Output filename (default: wallmapper.png)
  --stats STATS         Print some raw statistics (default: True)
```

They are all optional and we provide defaults for all of them.

By default, we generate wallpapers centered in Washington, DC using the amazing [woodcut basemap](https://www.mapbox.com/blog/interactive-woodcut-map/) from Eleanor Lutz.

## Examples

See the `Makefile` and the images in the `examples` directories for some nice basemaps at different zoom levels.

![woodcut](https://raw.github.com/zugaldia/wallmapper/master/examples/eleanor-woodcut-18.png)

![nightvision](https://raw.github.com/zugaldia/wallmapper/master/examples/dc-nightvision-16.png)

![space](https://raw.github.com/zugaldia/wallmapper/raw/master/examples/dc-nightvision-16.png)

## Troubleshooting

The scripts requires PIL to be installed and visible in the Python PATH. You may need to do something like the following:

```
$ export PYTHONPATH=$PYTHONPATH:/usr/local/lib/python2.7/site-packages
```

## Credits

The awesome folks from [Mapbox](http://www.mapbox.com) deserve all the credit for all the beautiful, open-data based, maps they produce.

## License

See `LICENSE`.
