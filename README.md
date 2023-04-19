# tpn_pc

Tatrzański Park Narodowy as point cloud web app

TODO:
- find vector of "TPN" borders - done
- acquire point clouds - partially done
- cut data to buffer - partially done
- create app.js with potree (?) blueprint - done

DEV LOG:

**DATA PROCESSING:**

At first I acquired open-source vector (shapefile) of every National Park in Poland. Point of interest is the Tatrzanski National Park (TPN). Using attributes (names of national parks), I removed all the others. Next I downloaded open-source point cloud data provided in equal-size tiles. All data that I acquired was cutted to the buffer (shapefile). The last optional part is cleaning water sheds from water (in my opinion that data is equal to noise), classification layer was very helpful in this process.

![[1.png]]

Lidar data are not updated from 2012 (ISOK project) and point clouds are "colored" by old/low-res ortophoto. And radiometry is unequal.

![[2.png]]

Some times ago I created very simple script in Python to coloring point cloud by georeferences - https://github.com/pnytko/cp_colorizer. 