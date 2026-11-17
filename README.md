# Countiles

Countiles are U.S. county tiles: every county of the contiguous United States divided into tiles of about 15 × 15 miles (about 24 × 24 km) that add up exactly to the county. They are meant for summarizing climate, soil and other gridded information at a resolution finer than the county while staying compatible with county statistics.

- `map/countiles.geojson`: the map, 13,140 tiles in 3,109 counties. Each tile has an `id` (county FIPS code and tile number, such as `20055-03`), its county, its area, and a center point (`lon`, `lat`) that is always inside the tile.
- `reference/`: the county boundaries the tiles are cut from (U.S. Census Bureau cartographic boundary file, 2023, 1:500,000).
- `countiles.ipynb`: the notebook that reads the reference counties and writes the map. The rules are in one function, `countiles(county)`.
- `docs/`: an interactive page to look at the map.

A tile can be as large as 20 × 20 miles and as small as 10 × 10 miles, and tile boundaries inside a county run north-south or east-west. Counties too small to divide are a single tile.
