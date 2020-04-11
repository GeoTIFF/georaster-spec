# georaster-spec
Work In Progress: Specification for GeoRaster, a Standardized Interface for Accessing In-Memory Geo-Enabled Raster Data

# required properties
| name | type | description |
| ---- | ---- | ----------- |
| noDataValue | number | no data value |
| pixelWidth | number | width of pixel in dimension of coordinate reference system |
| pixelHeight | number | height of pixel in dimension of coordinate reference system |
| projection  | number | [EPSG Code](https://en.wikipedia.org/wiki/EPSG_Geodetic_Parameter_Dataset), which designates the projection |
| width | number | number of pixels wide raster is |
| xmax | number | xmax in crs, which is often in longitude |
| xmin | number | xmin in crs, which is often in longitude |
| ymin | number | ymin in crs, which is often in latitude |
| ymax | number | ymax in crs, which is often in latitude |
| wkt  | string | [Well-known text representation of coordinate reference system](https://en.wikipedia.org/wiki/Well-known_text_representation_of_coordinate_reference_systems) |

# optional properties
| name | type | description |
| ---- | ---- | ----------- |
| maxs | 1-dimensional array of numbers | array with max value for each band |
| mins | 1-dimensional array of numbers | array with min value for each band |
| ranges | 1-dimensional array of numbers | array with difference between max and min value for each band |

# functions / methods
| name | return type | description |
| ---- | ---- | ----------- |
| getValues | 3-dimensional array of numbers | get the pixel values of the georaster in a multi-dimensional array, by band, row, and column |
| toCanvas | HTML Canvas Element | returns a canvas picture of the data.  You can pass in options object with height or width specified |
| toGeoTIFF | GeoTIFF ArrayBuffer | returns a GeoTIFF in ArrayBuffer format |
| toJPG | JPG ArrayBuffer | return a JPEG Image in ArrayBuffer format |
| toPNG | PNG ArrayBuffer | returns a PNG Image in ArrayBuffer format |

# Contribute
You are most welcome to contribute.  Check out our [CONTRIBUTING.md](CONTRIBUTING.md) for more info.
