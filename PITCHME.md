---?video=https://data.cyverse.org/dav/iplant/commons/cyverse_curated/Gillan_et_al_RAMA_2019/raw_images/Phantom_images_plot4_28Sept2016/DJI_0011.MP4

@snap[south span-100 text-center text-white]
## Processing Large sUAS datasets on HPC and data hosting on Cloud
@snapend

---

@snap[west span-50 text-green]
@css[](This talk **IS** for you if you are )
@ol[]
- flying sUAS 
- processing sUAS data
- mapping or doing analysis with sUAS data products
@olend
@snapend

@snap[east span-50 text-yellow]
@css[](If this talk **is NOT** for you)
@ol[]
- pretend you know this stuff already
- intimidate others by nodding thoughtfully
- count memes, quiz at the end
@olend
@snapend

---?color=linear-gradient(180deg, white 30%, #567AD2 50%)

@snap[north-west span-33]
<img src="https://i.imgur.com/etrjhje.jpg" height="100">
@snapend

@snap[west span-33 fragment]
@box[bg-green text-white rounded box-padding](Pro # Widely Used, Network & HPC)
@snapend

@snap[south-west span-33 fragment]
@box[bg-orange text-white rounded box-padding](Con # Training, $$$ floating licenses)
@snapend

@snap[north span-33]
<img src="https://images.ctfassets.net/go54bjdzbrgi/1ingG3f6HsI6i2qIuYe2cc/f0b4a12cb3a7ba6df067577009d32c3f/Pix4D_LOGO_MAIN_1024.png" height="100">
@snapend

@snap[midpoint span-33 fragment]
@box[bg-green text-white rounded box-padding](Pro # Ready to use, ESRI integration)
@snapend

@snap[south span-33 fragment]
@box[bg-orange text-white rounded box-padding](Con # less scalable, $$$ for Cloud)
@snapend

@snap[north-east]
<img src="https://pbs.twimg.com/profile_images/578011545969389568/qrV14aGg.png" height="100">
@snapend

@snap[east span-33 fragment]
@box[bg-green text-white rounded box-padding](Pro # Free, nice interface)
@snapend

@snap[south-east span-33 fragment]
@box[bg-orange text-white rounded box-padding](Con # less accurate, less scalable)
@snapend

---?color=linear-gradient(80deg, white 50%, #567AD2 50%)

@snap[east span-40 text-white]
@fa[quote-left quote-graphql](Why do I need to process sUAS data on the HPC?)
<img src="https://polomania.hu/images/designs/tn_orig/PM01180/12639.png" height="200">
@snapend

@snap[north-west span-40 fragment text-blue]
@box[](Reason 1. Time is our most valuable resource # Have you ever done an SfM-MVS reconstruction of 10,000+ 20 megapixel images?)
@snapend

@snap[south-west span-40 fragment text-blue]
@box[](Reason 2. Scale Limitation # You fly sUAS every X (day, week, month) across N (plots, fields, sites))
@snapend

---?color=linear-gradient(80deg, white 50%, #567AD2 50%)

@snap[east span-50 font-montserrat text-white]
@fa[quote-left quote-graphql](Working on HPC is easy!)
@snapend

@snap[north-west span-40 fragment text-blue]
@box[](Task 1. # Create an HPC Account)
@snapend

@snap[west span-40 fragment text-blue]
@box[](Task 2.  # Move your data to the scratch system)
@snapend

@snap[south-west span-40 fragment text-blue]
@box[](Task 3. # Request some worker nodes and go!)
@snapend

@snap[north-east fragment span-50]
@fa[text-06 font-montserrat](*Narrator Voice - "It was not easy*")
<img src="https://media.giphy.com/media/3oriNNwSR4ET5zd0xq/giphy.gif" height="300">
@snapend

@snap[south-east fragment span-40]
@fa[text-06 font-montserrat](*but its FREE*")
<img src="https://media.giphy.com/media/916t1VsCg2qoo/giphy.gif" height="100">
@snapend

---?image=assets/imagery/metashape_hpc.jpeg&size=contain


---

@snap[west fragment span-40 font-montserrat text-05]
@css[](Load Singularity)
<img src="https://media.giphy.com/media/3o85xAwT5hvVXhyuli/giphy.gif" height="150">
@snapend

@snap[north-west fragment span-40 font-montserrat text-05]
@css[](Start Graphic User Interface)
<img src="https://media.giphy.com/media/3rgXBEi3D9MjNONsm4/giphy.gif" height="150">
@snapend

@snap[north-east fragment span-40 font-montserrat text-05]
@css[](Request Worker Nodes)
<img src="https://media.giphy.com/media/yoJC2GGW98YQY2a8PS/giphy.gif" height="150">
@snapend

@snap[north fragment span-40 font-montserrat text-05]
@css[](Start Monitor)
<img src="https://media.giphy.com/media/rN3Xp323XRxV6/giphy.gif" height="150">
@snapend

@snap[midpoint fragment span-40 font-montserrat text-05]
@css[](Start Server node)
<img src="https://media.giphy.com/media/YBbiSlb0IzC24/giphy.gif" height="150">
@snapend

@snap[east fragment span-40 font-montserrat text text-05]
@css[](Load images and create project)
<img src="https://media.giphy.com/media/3nMyrWq4bQwPm/giphy.gif" height="150">
@snapend 

@snap[south fragment span-100]
```bash
$ module load singularity
$ ./metashape-pro/metashape.sh 
$ ./metashape-pro/monitor.sh 
$ singularity run metashape_container.sif ./metashape-pro/metashape.sh --node 
$ ./metashape-pro/metashape.sh --server
$ python3 quick_layout.py 
```
@[1](Load Singularity)
@[2,3](Start Graphic User Interface and Monitor)
@[4,5](Start Server & Worker nodes)
@[6](Load and process images)

---

## HPC Documentation

hpc.arizona.edu

---

Working with Data in the Cloud

---

@snap[west span-50 fragment text-white]
@box[](sUAS Data)
@ol[text-08]
- Mission Flight Plan & Logs (*.gpx, .geojson, .shp*)
- Images, Videos (*.dng, .jpeg, .raw, .png, .tiff*)
- Ground Control Points (*.csv, .xyz, .txt, .gpx*)
@olend
@snapend

@snap[east span-50 fragment text-white]
@box[](Derivatives)
@ol[text-08]
- Orthomosaics (*.mbtiles, .tif*)
- Point Clouds (*.laz, .ept*)
- Digital Elevation Models | Digital Terrain Models (*.tif*)
@olend
@snapend

---

CyVerse Data Store

---?color=linear-gradient(80deg, white 50%, #567AD2 50%)
