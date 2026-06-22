# India Voluntary Carbon Market Explorer: indiavcm.com
## An inventory of every carbon offset project across India.

### 1. About This Dashboard
This dashboard maps India's voluntary carbon market projects as a geospatial inventory. Each mapped project appears as a point, with filters for registry, BCTP scope category, status, vintage year, and issued credits. Projects without usable coordinates are not drawn on the map, but remain available in the Data tab and can be isolated with the Map Location filter.

### 2. Data Sources
Project records, credit volumes, methodologies, and status fields come from the Berkeley Carbon Trading Project (BCTP) Voluntary Registry Offsets Database. Project geometries were enriched from registry geometry files, registry-reported coordinates, spatial joins, and text-based location resolution where needed.

### 3. Geographic Methodology
Each mapped project carries provenance tags describing how its coordinate and administrative location were obtained. Higher precision sources include official registry point locations and boundary-polygon centroids; lower precision sources include district- or state-level estimates where the source record gives limited location detail.

Coordinate quality flags distinguish clean coordinates from near-offshore, corrected, or flagged coordinates. These flags are shown in project detail panels and in the glossary below for transparency.

### Coordinate Source Glossary
`Technical tag` Plain-English meaning

`BAD_COORD`	Coordinate appears wrong or unreliable and is flagged
`NEAR_OFFSHORE`	Coordinate is just offshore but plausibly associated with the project area
`NOT_SITE_SPECIFIC`	Broad KML footprint; not site-specific enough for a map point
`NO_COORDINATE`	No reliable project coordinate was available
`OK`	Coordinate passed dashboard quality checks
`PLACEHOLDER`	Coordinate appears to be a placeholder or shared default
`SIGN_FIXED`	Coordinate sign appeared wrong and was corrected
`SWAP_FIXED`	Latitude and longitude appeared reversed and were corrected
`api_centroid`	Provided directly by the registry data system
`api_centroid_corrected_lat_lon_swap`	Provided by the registry after correcting a latitude/longitude swap
`api_reported_standalone`	Reported by the registry as a standalone project coordinate
`broad_kml_not_district_resolvable`	Broad KML footprint; not resolvable to a single district
`geocoded`	Estimated from the project written location description
`geocoded_district_near_centroid`	Estimated near the center of the named district, due to limited location detail
`geocoded_state_near_centroid`	Estimated near the center of the named state, due to limited location detail
`implausible_uncorrectable`	Source coordinate was implausible and could not be corrected reliably
`kml_point`	Marked with the project official point location
`kml_point_centroid_reduced`	Marked with the project official point location, simplified for web display
`kml_polygon`	Estimated from the project official boundary polygon
`kml_polygon_centroid_reduced`	Estimated from the project official boundary polygon, simplified for web display
`kml_polygon_not_site_specific`	Official KML footprint was too broad to represent as a site-level point
`manual`	Manually verified by the dashboard maintainer
`no_coordinate`	No coordinate available in the source data
`none`	None
`not_locatable`	No reliable mappable location could be resolved
`not_mapped_broad_kml_footprint`	Not mapped because the source KML footprint was too broad for a site-level coordinate
`not_mapped_no_coordinate`	Not mapped because no reliable coordinate was available
`spatial_join_district`	Assigned to a district using a spatial join of the mapped coordinate
`spatial_join_district_buffered`	Assigned to a nearby district using a small boundary buffer
`spatial_join_state`	Assigned to a state using a spatial join of the mapped coordinate
`text_match`	Matched from text in the project description
`text_matched_existing`	Matched from project text to an existing named location
`unlocated_multi_state`	Unlocated Multi State
`unresolved`	Could not be resolved to a reliable administrative location

### 4. Scope and Category System
The dashboard uses the eight BCTP-native scope values directly: Renewable Energy, Household & Community, Agriculture, Forestry & Land Use, Industrial & Commercial, Waste Management, Transportation, Chemical Processes. These are carried through unchanged from the BCTP source database rather than collapsed into a custom dashboard taxonomy. Because the categories remain BCTP-native, category counts in this dashboard are directly comparable to other BCTP-based analyses.

### 5. Data Limitations
Vintage year coverage is partial. Vintage-year charts should be read as lower-bound indicators where projects do not report a first vintage year.

Locatability differs by registry. Some projects, especially records without usable registry geometry or location detail, cannot be placed on the map. They remain included in all non-geospatial totals and charts, and can be filtered in the Data tab under Map Location.
Coordinate quality varies. Some source coordinates required repair, and some remain flagged as unreliable or approximate.
Status uses a hierarchy. Registry-specific status fields are preferred, with BCTP snapshot status used as a fallback.
Aggregated programmes can share coordinates. Bundled or programmatic activities may report one coordinate for many underlying sites.

### 6. Cite This Dashboard
`Shubham Love, India Voluntary Carbon Market Explorer, June 2026, https://probablyshubham.github.io/india-vcm-explorer/`

### 7. Underlying Data Sources
This dashboard is built on the BCTP Voluntary Registry Offsets Database. Please acknowledge the underlying data source separately from the dashboard citation when using the project data.

`Pamela Quartson, Barbara K Haya, Tyler Bernard, Aline Abayo, Xinyun Rong, Ivy S So, Micah Elias. (2026). Voluntary Registry Offsets Database v2026-04, Berkeley Carbon Trading Project, University of California, Berkeley. Retrieved from: https://gspp.berkeley.edu/berkeley-carbon-trading-project/offsets-database.`
