# WEEK 3
## Advanced Visualizations and Geospatial Data
* Waffle Charts
	* A waffle chart is an interesting visualization that is normally created to display progress toward goals.
	* Is basically a square display, usually consisting of 100 smaller squares arranged in a 10-by-10 layout..
	* `pywaffle`
* Word Clouds
	* A word cloud is depiction of the frequency of different words in some textual data.
* Seaborn and Regressin Plots
	* Seaborn is python visualization library based on Matplotlib.
```
import seaborn as sns
ax = sns.regplot(x='year', y='total', data=df_tot, color='green', marker='+')
```
* Introduction to Folium
	* Folium is a powerful Python library that helps you create several types of Leaflet maps.
	* It enables both the binding of data to a map for choropleth visualizations as well as passing visualizations as markers on the map.
```
# define the world map center around canada
world_map = folium.Map(
		location=[56.130, -106.35],
		zoom_start=4,
		tiles='Stamen Toner'
	)

# display world map
world_map
```
* Maps with Markers
	* Superimpose on top of the visualiztion (folium library)
```
# define the world map center around canada
world_map = folium.Map(
		location=[56.130, -106.35],
		zoom_start=4,
		tiles='Stamen Toner'
	)

# add a red marker to Ontario
# create a fearure group
ontatio = folium.map.FeatureGroup()

# style the feature group
ontario.add_child(
	folium.feature, CircleMarker(
	[51.25, -85.32], radius = 5,
	color = 'red', fill_color = 'Red'
	)	
)

# add the fearure group to the map
canada_map.add_child(ontario)

# label the marker
folium.Marker([51.25, -85.32],
	popup='Ontario').add_to(canada_map)

# display map
canada_map
```
* Choropleth Maps
	* Is a type of thematic map in which a set of pre-defined areas is coloured or patterned in proportion to a statistical variable that represents an aggregate summary of a geographic characteristic within each area.
```
# create a plain world map
world_map = folium.Map(
	zoom-start=2,
	tiles='Mapbox Bright'
)

## geojson file
world_geo = r'world_countries.json'

# generate choropleth map using the total
# pouplatin of each country to Canada from
# 1980 to 2013
world_mpa.choropleth(
	geo_path=world_geo,
	data=df_canada,
	columns=['Country', 'total'],
	key_on='feature.properties.name',
	fill_color='YlOrRd',	
	legend_name='Immigration to Canada'
)

#display map
world_map
```
