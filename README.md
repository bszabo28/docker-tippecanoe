# Telepítés
```sh
docker-compose build
```

# Futtatás
```sh
docker-compose run tippecanoe tippecanoe -s EPSG:4326 -pi -f -z13 -o osm-vector-dunaujvaros.mbtiles  \
geojson/osm-places.geojson \
geojson/osm-aeroways.geojson \
geojson/osm-amenities.geojson \
geojson/osm-barrierpoints.geojson \
geojson/osm-barrierways.geojson \
geojson/osm-housenumbers-interpolated.geojson \
geojson/osm-housenumbers.geojson \
geojson/osm-housenumbers-interpolated.geojson \
geojson/osm-road.geojson osm-buildings.geojson \
geojson/osm-landusage.geojson \
geojson/osm-transport-areas.geojson \
geojson/osm-waterareas.geojson \
geojson/osm-waterways.geojson
```