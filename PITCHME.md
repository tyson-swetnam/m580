---?color=linear-gradient(180deg, #2D2926 30%, #000000 50%)

@snap[south span-100 text-center font-montserrat text-white text-14]
@fa[quote-graphql](Processing Large sUAS datasets on HPC and data hosting on Cloud)
@snapend

---

@snap[west span-50 text-white]
@css[](This talk IS for you if you are )
@ol[]
- flying sUAS 
- processing sUAS data
- mapping or doing analysis with sUAS data products
@olend
@snapend

@snap[east span-50 text-white]
@css[](If this talk is NOT for you)
@ol[]
- pretend you know this stuff already
- intimidate the others by nodding thoughtfully
- count memes, quiz at the end
@olend
@snapend

---?color=linear-gradient(180deg, white 30%, #567AD2 50%)

@snap[north-west span-33]
<img src="https://i.imgur.com/etrjhje.jpg" height="100">
@snapend

@snap[west span-33 text-07 fragment font-montserrat text-white]
@css[](Pros)
@ol
- Wide Adoption by Surveyors and Researchers
- Network Processing on Cloud and HPC
- Cheaper than others
@olend
@snapend

@snap[south-west span-33 text-07 fragment font-montserrat text-white]
@css[](Cons)
@ol
- Requires some training
- $$$ for floating licenses
@olend
@snapend

@snap[north span-33]
<img src="https://images.ctfassets.net/go54bjdzbrgi/1ingG3f6HsI6i2qIuYe2cc/f0b4a12cb3a7ba6df067577009d32c3f/Pix4D_LOGO_MAIN_1024.png" height="100">
@snapend

@snap[span-33 text-07 fragment font-montserrat text-white]
@css[](Pros)
@ol
- Ready to use
- Automation and integration
- ESRI Drone2Map
@olend
@snapend

@snap[south span-33 text-07 fragment font-montserrat text-white]
@css[](Cons)
@ol
- Less flexible
- $$$$ for Cloud Computing
@olend
@snapend

@snap[north-east]
<img src="https://static.wixstatic.com/media/c0136c_970bb6ac4fdc47aca453859e71abe7cc~mv2.png" height="100">
@snapend

@snap[east span-33 text-07 fragment font-montserrat text-white]
@css[](Pros)
@ol
- Free
- Easy to use, nice interface
@olend
@snapend

@snap[south-east span-33 text-07 fragment font-montserrat text-white]
@css[](Cons)
@ol
- Less accurate than Metashape or Pix4D
- Does not perform at scale 
@olend
@snapend

---?color=linear-gradient(80deg, white 50%, #567AD2 50%)

@snap[east span-40 text-center font-montserrat text-white text-14]
@fa[quote-left quote-graphql](Why do I need to process sUAS data on the HPC?)
<img src="https://polomania.hu/images/designs/tn_orig/PM01180/12639.png" height="200">
@snapend

@snap[north-west span-40 text-08 fragment font-montserrat text-blue]
@box[](Reason 1. Time is our most valuable resource # Have you ever done an SfM-MVS reconstruction of 10,000+ 20 megapixel images?)
@snapend

@snap[south-west span-40 text-08 fragment font-montserrat text-blue]
@box[](Reason 2. Scale Limitation # You fly sUAS every X (day, week, month) across N (plots, fields, sites))
@snapend

---?color=linear-gradient(90deg, white 50%, #567AD2 50%)

@snap[east span-40 text-center font-cabin text-white]
@fa[quote-left quote-graphql](Using the HPC is easy!)
@snapend

@snap[north-east fragment text-center span-45 text-07 font-montserrat]
@fa[](*Narrator Voice : "It was not easy...*")
<img src="https://media.giphy.com/media/3oriNNwSR4ET5zd0xq/giphy.gif" height="200">
@snapend

@snap[south-east fragment text-center span-45 text-07 font-montserrat]
@fa[](*"but it is _FREE_"*)
@snapend

@snap[north-west span-40 text-07 fragment font-montserrat text-blue]
@box[](Task 1. # Create an HPC Account)
@snapend

@snap[west span-40 text-07 fragment font-montserrat text-blue]
@box[](Task 2.  # Move your data to the scratch system)
@snapend

@snap[south-west span-40 text-07 fragment font-montserrat text-blue]
@box[](Task 3. # Request some worker nodes and go!)
@snapend

---?image=assets/imagery/metashape_hpc.jpeg&size=contain

---

# HPC Documentatation

---

Data Management

---

@snap[west span-50 text-center fragment font-montserrat text-white text-14]
@box[](sUAS Core Data)
@ol[text-08]
- Mission Flight Plan & Logs (.gpx, .geojson, .shp)
- Images, Videos (.dng, .jpeg, .raw, .png, .tiff)
- Ground Control Points (.csv, .xyz, .txt, .gpx)
@olend
@snapend

@snap[east span-50 text-center fragment font-montserrat text-white text-14]
@box[](sUAS Derivative Data)
@ol[text-08]
- Orthomosaics 
- Point Clouds
- Digital Elevation Models | Digital Terrain Models
@olend
@snapend

---?color=linear-gradient(80deg, white 50%, #567AD2 50%)

Workflow Managers

---

CyVerse

---?color=linear-gradient(80deg, white 50%, #567AD2 50%)
