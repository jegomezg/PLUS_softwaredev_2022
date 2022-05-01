# Assigment .yml
## Creation and activation of new enviornment 


```
conda create --name SD2022_geoenv
conda activate SD2022_geoenv
```


## Installing packages
The enviorment will rely two projects: 

* [sarsen](https://github.com/bopen/sarsen) - A library to process raw sentinel-1 data with geocoding and gamma filtering workflows. This is installed with conda-forge


```
conda install -c conda-forge dask proj-data sarsen
```


* [python-geospatial](https://github.com/giswqs/python-geospatial) - A project that contains several (almost all) geospatial libraries for python. This will be installed through the yml provided in the project, updating the enviorment.
 
```
git clone https://github.com/giswqs/python-geospatial.git
conda env update -n SD2022_geoenv --file environment.yml
```
#Exporting .yml and requirements txt file.

Exporting yml
```
geoenv.yml
```

Exporting txt
```
requirements.txt
```
Making env avaliable in notebook
```
python -m ipykernel install --user --name=geoenv
```

#Commiting files
 ```
git add geoenv.yml requirements.txt
git status
git commit .
git push origin main
```

