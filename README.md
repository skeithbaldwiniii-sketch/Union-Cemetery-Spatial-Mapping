# Union-Cemetery-Spatial-Mapping
## Cemetery Spatial Mapping in Leesburg, Loudoun County, VA
Built a georeferenced spatial dataset by converting field-collected coordinate data into features, digitizing plots, and applying spatial joins to classify and validate cemetery sections 

This started as my final project for when I completed Geographical Information Systems II in December 2025. This is one I am actively continuing to extend to an internship. 

I was looking for data and ideas for my Introduction to Remote Sensing final project and was looking at cemeteries since they tend to change/ grow over time. I discovered that the cemetery data on the Loudoun Geohub had cemeteries in a layer as points rather than a polygon, which would make more sense given the extent of the cemeteries. With this in mind, I thought it would be a good idea to plot and map out Union Cemetery, which is the biggest cemetery in Loudoun County, specifically in Leesburg.

<img width="632" height="588" alt="image" src="https://github.com/user-attachments/assets/2ce065f8-254b-4120-bb48-4a9888c4e262" />


I also downloaded the parcels and road casing of Loudoun county from the Loudoun Geohub to isolate the specific area of land I was researching. I used “make layer from selected feature” on the specific parcel of interest and used the clip tool to clip the road casings to the parcel

<img width="632" height="588" alt="image" src="https://github.com/user-attachments/assets/8e14e7db-23fa-4de2-b89e-db59d7374e06" />


To start, I visited the cemetery and used the google maps drop a pin feature to mark the gravestone that was at the end of each row. This would give me guideposts to determine where plots start and end, with using the names on the edges, while also allowing me to be respectful and not walk on the grass at the cemetery. 

<img width="442" height="412" alt="image" src="https://github.com/user-attachments/assets/b63d1bf1-6af4-428b-8ffc-4e4e0aaaf6ad" />


I downloaded the point data using google takeout, which gave me a csv formatted spreadsheet with all of the points. Since the point data is formatted as a URL, rather than having two separate cells dedicated to an X point and a Y point, I consulted chat gpt. I placed 530 points, so finding a quicker way to do this rather than manually splitting the URL into the 2 cells felt optimal. 

<img width="619" height="148" alt="image" src="https://github.com/user-attachments/assets/66c0b22f-1c5c-4d4a-a45d-c969d81c8cd0" />

<img width="585" height="367" alt="image" src="https://github.com/user-attachments/assets/39141395-9612-4193-a76f-d6b8e58082df" />

<img width="619" height="137" alt="image" src="https://github.com/user-attachments/assets/a97fd206-d62f-4ea0-bbbc-7d8e74711eb4" />

<img width="585" height="302" alt="image" src="https://github.com/user-attachments/assets/602f0f34-735c-4af2-9b2e-a467353853d7" />


I then visited the Thomas Balch library in Leesburg, VA, which specializes in historical referencing and research and used the 2 books they had on the cemetery to locate the plots for all of the names that I recorded, as well as the section in which the gravestone was located. 

I uploaded this csv to ArcGIS pro and used the XY table to point tool to generate data points, and adjusted the symbology based on section to get an idea of the division & barrier of each section.

<img width="280" height="377" alt="image" src="https://github.com/user-attachments/assets/da0fe7af-7c88-421c-bd2c-d1dd9974e961" />

<img width="619" height="444" alt="image" src="https://github.com/user-attachments/assets/4506557e-376e-41d2-992d-0128908ba82d" />

<img width="511" height="341" alt="image" src="https://github.com/user-attachments/assets/cb08a422-3bbb-4a14-b18d-8f8bd35808bc" />


From there, I decided to try and use the machine learning tool to identify all of specific grave stones and their points. I used both NAIP imagery, and High Resolution orthoimagery, the latter of which looked like it would yield better results based on how it look. I got further in the steps with NAIP, but the tool proved to be unsuccessful due to the size of the grave stones. 

<img width="535" height="437" alt="image" src="https://github.com/user-attachments/assets/31a469b3-1427-4b80-99cb-20f06e123d7c" />

<img width="350" height="488" alt="image" src="https://github.com/user-attachments/assets/105007f7-9f94-4056-84af-f7fac8eeb3e3" />

<img width="262" height="416" alt="image" src="https://github.com/user-attachments/assets/4d104262-a3d6-426a-8be6-e9c36ee1e344" />

<img width="708" height="596" alt="image" src="https://github.com/user-attachments/assets/ae7bf0f2-c648-4b97-ae3e-2dca4cc807b1" />

<img width="585" height="358" alt="image" src="https://github.com/user-attachments/assets/6a6a0a83-5e4d-4c16-8dc4-2f1ce6ab9c26" />

<img width="290" height="488" alt="image" src="https://github.com/user-attachments/assets/77346a20-038c-4116-b23d-b055b20b1071" />

<img width="290" height="526" alt="image" src="https://github.com/user-attachments/assets/a7f301ae-8b6e-445d-aa69-fe47051658af" />

<img width="290" height="466" alt="image" src="https://github.com/user-attachments/assets/2b3881f1-2bbb-4494-a425-330df8e2f210" />

<img width="698" height="413" alt="image" src="https://github.com/user-attachments/assets/8b732be3-4f49-46aa-96df-e044f64e7ae6" />


Also briefly tried a laz file, but it’s also not worth mentioning since again the gravestones are undetectable.

<img width="820" height="413" alt="image" src="https://github.com/user-attachments/assets/5a013885-412a-4361-a222-0cea1cc5426a" />


I called the cemetery office to see if they had any more resources for me, and they gave me 3 up to date blue prints of the cemetery complete with all of the plot numbers. I georeferenced this and began the next step.

<img width="619" height="488" alt="image" src="https://github.com/user-attachments/assets/53433310-dcb4-41ee-968d-1b0a6c6d633a" />

<img width="505" height="325" alt="image" src="https://github.com/user-attachments/assets/1ab71ddb-58a0-4ab2-b7de-6ea2e0091091" />

<img width="401" height="321" alt="image" src="https://github.com/user-attachments/assets/5a30fe0e-1d9d-4c7b-a7eb-b86c2c16fb2d" />



Using create feature class, I drew every lot using the map as a guide. 

<img width="590" height="413" alt="image" src="https://github.com/user-attachments/assets/7bce8277-7708-4778-b302-287b7a594e51" />

Used the point data I collected previously as guideposts to how each plat was divided and is classified

<img width="634" height="413" alt="image" src="https://github.com/user-attachments/assets/978dbb9a-a9a4-4db4-a6fc-1dd1477bf621" />


I also used spatial join to verify the guideposts for the division of plats. If I was able to take the time, I would manually move the points to which plat I recorded from the book and make the picture more clear. Though it is still just limited to the data from the book, so the information is dated. 

<img width="262" height="488" alt="image" src="https://github.com/user-attachments/assets/be353668-2ab3-4578-b3ef-02fb8b678845" />

<img width="745" height="502" alt="image" src="https://github.com/user-attachments/assets/0b038f5e-4c4f-4a5a-bcad-c34de0e66345" />


I then added a column in the attribute table and defined as "lot," which I manually edited lot by lot to reflect the number of the lot. I am now currently transcribing the books written by Elizabeth Frain, both titled Union Cemetery, and entering all of the names published in the books. As of now, I am including Plat, Lot, Name (Last, First, Middle), birth date, death date, how they died, where they died, when they were buried, and their age. Not every name includes this information, but this is taking me some time. 

In the meantime, enjoy a 1844 drawing of Union Cemetery that was given to me by Thomas Balch Library in Leesburg, VA. 
<img width="550" height="373" alt="image" src="https://github.com/user-attachments/assets/8bbef644-b217-44a0-9e5a-fe4b7fb98bbd" />

<img width="559" height="383" alt="image" src="https://github.com/user-attachments/assets/d571e525-088f-4473-bf06-573428435c21" />


Book Sources:
Frain, Elizabeth R. Union Cemetery: Leesburg, Loudoun County, Virginia. Plats A&B 1784-1995. Willow Bend Books, 1995.
Frain, Elizabeth R. Union Cemetery: Leesburg, Loudoun County, Virginia. The Later Plats 1880-1995. Willow Bend Books, 1997.



