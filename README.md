# georaster-spec
Work In Progress: Specification for GeoRaster, a Standardized Interface for Accessing In-Memory Geo-Enabled Raster Data

# required properties
| name | type | description |
| ---- | ---- | ----------- |
| noDataValue | number | no data value |
| pixelWidth | number | width of pixel in dimension of coordinate reference system |
| pixelHeight | number | height of pixel in dimension of coordinate reference system |
| projection | { code, wkt } | object that holds two properties, the epsg code and well known text representation of the projection |
| width | number | number of pixels wide raster is |
| xmax | number | xmax in crs, which is often in longitude |
| xmin | number | xmin in crs, which is often in longitude |
| ymin | number | ymin in crs, which is often in latitude |
| ymax | number | ymax in crs, which is often in latitude |

# optional properties
| name | type | description |
| ---- | ---- | ----------- |
| values | 3-dimensional array of numbers | two dimensional array of pixel values (for Cloud Optimized GeoTIFF's, use `getValues` instead)  |
| maxs | 1-dimensional array of numbers | array with max value for each band |
| mins | 1-dimensional array of numbers | array with min value for each band |
| ranges | 1-dimensional array of numbers | array with difference between max and min value for each band |

# functions / methods
| name | return type | description |
| ---- | ---- | ----------- |
| getValues | 3-dimensional array of numbers | described above |
| toCanvas | HTML Canvas Element | returns a canvas picture of the data.  You can pass in options object with height or width specified |

# Contribute
You are most welcome to contribute.  Check out our [CONTRIBUTING.md](CONTRIBUTING.md) for more info.
