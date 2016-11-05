# :cat: RefleCats
b/c reflections mattersヽ(^‥^=ゞ)

repository for [Copernicus](copernicus.devpost.com) 4-5/11/2016 hackathon in Vienna, Austria

### Setup
before first pull you need [Git LFS](https://git-lfs.github.com/) installed (b/c tif)
```
brew install git-lfs
git lfs install
```
Query hints for [scihub](https://scihub.copernicus.eu/dhus/)
* Linz S2A_OPER_PRD_MSIL1C_PDMC swaths
  * `platformname:Sentinel-2 footprint:"intersects(48.2949799,14.1873221)"`
* Vienna S2A_OPER_PRD_MSIL1C_PDMC swaths
  * `platformname:Sentinel-2 footprint:"intersects(48.2082,16.3738)"`


### Technology Part

### Data acquisition

At [Scihub](https://scihub.copernicus.eu/dhus/) we used query for Vienna
```
platformname:Sentinel-2 footprint:"intersects(48.2082,16.3738)"
```

to get proper file names of data from Sentinel 2, which we unziped and loaded into qGIS

#### Data processing

[Convert Landsat DNs to albedo](http://yceo.yale.edu/how-convert-landsat-dns-albedo)
![img](http://yceo.yale.edu/sites/default/files/images/AlbedoForm.PNG)

i.e. use this formula can be implemented in ENVI using Band Math as:
```
((0.356*B1) + (0.130*B2) + (0.373*B3) + (0.085*B4) + (0.072*B5) -0.018) / 1.016
```

#### Web

* Leaflet

#### Mobile

* Xamarin
* Mapbox
