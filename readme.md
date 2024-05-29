**Run BE
cd BE
osrm-extract data/south-korea-latest.osm.pbf
osrm-partition data/south-korea-latest.osm
osrm-customize data/south-korea-latest.osrm
osrm-routed --algorithm=MLD data/south-korea-latest.osrm 

**Run FE
cd FE
npm i
npm run compile
npm run start-index