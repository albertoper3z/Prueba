# Modelos Epidemiológicos
## Detectives
### Políticas Públicas
```
import pandas as pd
import geopandas

df=geopandas.read_file('mexican_states.geojson')
d1=df.iat[5,-1]
d2=df.iat[7,-1]

m=folium.Map(location=[26, -99.156], zoom_start=4.5)
folium.GeoJson(d1,name='geojson').add_to(m)

style2 = {'fillColor': '#8A2BE2', 'color': '#FF7F50'}
folium.GeoJson(d2,name='geojson',style_function=lambda x:style2).add_to(m)
m
   
```
