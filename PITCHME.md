---?video=https://data.cyverse.org/dav-anon/iplant/commons/cyverse_curated/Gillan_et_al_RAMA_2019/raw_images/Phantom_images_plot4_28Sept2016/DJI_0011.MP4

@snap[south span-100 text-center text-white]
## ~Fire~ Technology is a good servant, but a bad master

---

# About me

- NPS Forestry technician 2002-2005
- USFS Fire Management Specialist 2008-2013

- Watershed Managment MS & PhD
- Speciality in GIS and Forest Disturbance Dynamics

- Research Assistant Professor of Geoinformatics at UA

---

# Briefing

- How technology can impact your job on a project fire
  - before
  - during
  - after

---

# Think about

- How technology can make your 
      job easier?
      people safer?
- How can technology help us create healthier, more resilient forests?

- How to avoid technology making your life harder
- How to avoid the dangers of overly relying on a technology 

---

## Big Data & Fourth Industrial Revolution

- Mobile apps
- Communication
- Vizualizaiton

---

# Act 1: Before the Fire

---

## 

---

# Act 2:During a Fire

---

## RX 

---

@snap[north-east span-33 text-center]
[@img[span-100](https://upload.wikimedia.org/wikipedia/commons/thumb/7/77/US-NationalWildfireCoordinatingGroup-Logo.svg/1200px-US-NationalWildfireCoordinatingGroup-Logo.svg.png)](https://www.nwcg.gov/sites/default/files/publications/pms515.pdf)
@snapend 

@snap[north-west span-33 text-center]
flying sUAS during a fire
@snapend

---
https://www.c4isrnet.com/unmanned/2019/09/05/what-can-the-military-learn-from-forest-fire-fighting-drones/

---

## Project Fires

---

## sUAS

https://upload.wikimedia.org/wikipedia/commons/thumb/7/77/US-NationalWildfireCoordinatingGroup-Logo.svg/1200px-US-NationalWildfireCoordinatingGroup-Logo.svg.png

---

## ArcGIS Pro, Survey 123

---

## Open Source GIS

QGIS

---

## Cell Phones & GPS

- communication
- Weather visualization
- Real time fire progression maps
- Location data

- inReach

---

## 

---

# Act 3: After a Fire

---

## sUAS Use Case: Camp Fire 2018

---

## BAER

---


---

# Act 4: Before the Next Fire

---

## Next Gen 911

---

## Fuels Monitoring

### sUAS SfM

---

### lidar

---

# After Action Review

What was the plan

What did I talk about?

What did you learn?

What could I do better next time?

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

---

@snap[west h3-white span-50]
### @fa[twitter] a recent informal survey of community members
@snapend

@snap[east span-50]
  @tweet[https://twitter.com/tommaso_jucker/status/1189847902673342464]
@snapend

---?color=linear-gradient(80deg, white 50%, #567AD2 50%)

@snap[east span-40 text-white]
@fa[quote-left quote-graphql](Why do I need to process sUAS data on the HPC?)
<img src="https://polomania.hu/images/designs/tn_orig/PM01180/12639.png" height="200">
@snapend

@snap[north-west span-40 fragment text-blue]
@box[](Reason 1. Time is our most valuable resource # Have you ever attempted a SfM-MVS reconstruction of 10,000+ 20 megapixel images?)
@snapend

@snap[south-west span-40 fragment text-blue]
@box[](Reason 2. Scale Limitation # You fly sUAS every X (day, week, month) across N (plots, fields, sites))
@snapend

---?color=linear-gradient(80deg, white 50%, #567AD2 50%)

@snap[east span-50 text-white]
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
<img src="https://media.giphy.com/media/916t1VsCg2qoo/giphy.gif" height="100">
@fa[text-06 font-montserrat](*but it is _FREE_*")
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
@css[](Start Network Monitor)
<img src="https://media.giphy.com/media/rN3Xp323XRxV6/giphy.gif" height="150">
@snapend

@snap[midpoint fragment span-40 font-montserrat text-05]
@css[](Start Server Node)
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

<canvas data-chart="bar">
<!--
{
 "data": {
  "labels": ["Your Laptop", " My Workstation"," El Gato"," Ocelote"," HPC-X", " AWS EC2 g4dn.16xlarge"],
  "datasets": [
   {
    "data":[4,16,16,28,96,64],
    "label":"CPU Cores",
    "backgroundColor":"rgba(20,20,220,.8)"
   },
   {
    "data":[16,128,64,168,256,256],
    "label":"CPU RAM (GB)",
    "backgroundColor":"rgba(120,120,220,.8)"
   }
  ]
 },
 "options": { "responsive": "true" }
}
-->
</canvas>

@snap[north-east fragment font-montserrat text-06]
$4.352 / hr
@snapend

---

<canvas data-chart="bar">
<!--
{
 "data": {
  "labels": ["Your Laptop", " My Workstation"," El Gato x 10 nodes"," Ocelote x 10 nodes"," HPC-X x 10 nodes", " AWS EC2 g4dn.16xlarge x 10 nodes"],
  "datasets": [
   {
    "data":[4, 16,160,280,960,640],
    "label":"CPU Cores",
    "backgroundColor":"rgba(20,20,220,.8)"
   },
   {
    "data":[16, 126,640,1680,2560,2560],
    "label":"CPU RAM (MB)",
    "backgroundColor":"rgba(120,120,220,.8)"
   }
  ]
 },
 "options": { "responsive": "true" }
}
-->
</canvas>

@snap[north-east fragment font-montserrat text-06]
$43.52 / hr
@snapend

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

---?image=assets/imagery/nifa.jpeg&size=contain

---?color=linear-gradient(80deg, white 50%, #567AD2 50%)

@snap[east span-40 text-white]
@fa[quote-left quote-graphql](Why should I use CyVerse?)
<img src="https://polomania.hu/images/designs/tn_orig/PM01180/12639.png" height="180">
@snapend

@snap[north-west span-40 fragment text-blue]
@box[](Reason 1. Computer time and data storage cost $$$$ # Do you host web services on AWS, or data on S3?)
@snapend

@snap[south-west span-40 fragment text-blue]
@box[](Reason 2. Location-Location-Location # Put your data in the same place that you intend to do work on them)
@snapend

@snap[south-east fragment span-40]
<img src="https://media.giphy.com/media/916t1VsCg2qoo/giphy.gif" height="100">
@fa[text-06 font-montserrat](*its FREE*")
@snapend

---
@snap[north span-100]
![GRAPHQL](/assets/imagery/cyverse_white.png)
@snapend

@snap[west span-33 text-white]
@box[](Data Store)
@ol[text-08]
- Host up to 10TB
- Cloud Storage
- Share with colleagues
@olend
@snapend

@snap[midpoint span-33 text-white]
@box[](Discovery Environment)
@ol[text-08]
- RStudio & Jupyter Notebooks
- Share Analyses
- Batch Processing
@olend
@snapend

@snap[east span-33 text-white]
@box[](Cloud Native Services)
@ol[text-08]
- Virtual Machines
- Run Jobs
- Run Services
@olend
@snapend

---

@snap[north span-100 text-center text-white text-14]
@fa[quote-graphql font-montserrat](Want to Learn More?)
@snapend

@snap[south span-100 text-center text-white text-14]
@fa[quote-graphql font-montserrat](Join Research Bazaar Arizona) 
<img src="https://pbs.twimg.com/profile_images/753651150222561280/lDw9oOzL.jpg" height="200">
@fab[windows fa-sm] @fab[r-project fa-sm] @fab[python fa-sm] @fab[docker fa-sm] @fab[slack fa-sm] @fab[apple fa-sm]  @fab[github fa-sm] @fab[linux fa-sm] @fab[ubuntu fa-sm] @fab[centos fa-sm] 
@fab[rebel fa-sm] @fab[confluence fa-sm] @fab[jenkins fa-sm] @fab[superpowers fa-sm] @fab[empire fa-sm] @fab[meetup fa-sm] @fab[twitter fa-sm] @fab[stack-overflow fa-sm] 
@snapend

@snap[west fragment]
@fa[coffee]
@fa[quote-graphql font-montserrat text-04](Tuesday 8-10AM BSRL Building)
@snapend

@snap[east fragment]
@fa[beer]
@fa[quote-graphql font-montserrat text-04](Thursday 4-6PM @Gentle Bens)
@snapend
