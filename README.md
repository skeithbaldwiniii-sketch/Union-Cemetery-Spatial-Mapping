# Union-Cemetery-Spatial-Mapping
<img width="590" height="413" alt="image" src="https://github.com/user-attachments/assets/7bce8277-7708-4778-b302-287b7a594e51" />
## Cemetery Spatial Mapping in Leesburg, Loudoun County, VA
This project focuses on building a georeferenced spatial dataset of Union Cemetery by combining field-collected data, historical records, and GIS-based digitization.

What started as a final project for Geographical Information Systems II (December 2025) has turned into an ongoing effort that I am continuing to expand.

## Project Motivation

While exploring potential project ideas, I noticed that cemetery data on the Loudoun GeoHub was represented as single points rather than full spatial extents. Given the size and structure of cemeteries, this felt incomplete.

That led me to map Union Cemetery in detail, with the goal of creating a more accurate and usable spatial dataset.

<img width="632" height="588" alt="image" src="https://github.com/user-attachments/assets/2ce065f8-254b-4120-bb48-4a9888c4e262" />

## Data Collection (Field + Historical)

I began by visiting the cemetery and collecting point data using Google Maps. Instead of walking across plots, I placed points at the ends of rows using visible headstones as reference markers. This allowed me to map the layout while remaining respectful of the space.

The data was exported using Google Takeout and converted into usable coordinates for ArcGIS.

To supplement this, I visited the Thomas Balch Library in Leesburg and used historical records to identify plot locations, section divisions, and associated names.

<img width="442" height="412" alt="image" src="https://github.com/user-attachments/assets/b63d1bf1-6af4-428b-8ffc-4e4e0aaaf6ad" /> 

## Initial Mapping

After converting the collected data into spatial points, I symbolized them by section to better understand how the cemetery was divided.

This gave me a rough structure of the cemetery layout, but it still lacked clearly defined plot boundaries.


## Attempted Automation (and why it didn't work)

I explored using imagery and machine learning tools to automatically detect gravestones using both NAIP and high-resolution imagery.

However, due to the small size and variability of gravestones, the results were unreliable. I also briefly explored LiDAR data, but it did not provide meaningful detection at this scale.

These attempts confirmed that manual digitization would be necessary for accuracy.


## Georeferencing & Digitization

I obtained up-to-date cemetery maps from the cemetery office and georeferenced them in ArcGIS.

Using these maps as a guide, I manually digitized each individual plot by creating a new feature class and drawing lot boundaries.

The point data I collected in the field was then used as guideposts to help verify section divisions and improve accuracy.

I also used spatial joins to validate how well the field-collected points aligned with the digitized plots.



<img width="619" height="488" alt="image" src="https://github.com/user-attachments/assets/53433310-dcb4-41ee-968d-1b0a6c6d633a" />

<img width="505" height="325" alt="image" src="https://github.com/user-attachments/assets/1ab71ddb-58a0-4ab2-b7de-6ea2e0091091" />

<img width="401" height="321" alt="image" src="https://github.com/user-attachments/assets/5a30fe0e-1d9d-4c7b-a7eb-b86c2c16fb2d" />


## Attribute Development

I added a “lot” field to the dataset and manually assigned lot numbers to each plot.

In parallel, I began building a more detailed attribute table using historical records. This includes:

- Section (Plat)
- Lot number
- Name (Last, First, Middle)
- Birth and death dates
- Burial information (when available)

This portion of the project is ongoing and represents a significant data entry effort.

<img width="1483" height="363" alt="image" src="https://github.com/user-attachments/assets/ab0c1ebc-0f77-420f-927e-5b65f4ac4c13" />


## Results & Current State

The result is a structured, georeferenced dataset of Union Cemetery that includes both spatial boundaries and associated historical information.

Compared to the original point-based dataset, this provides a much more accurate representation of the cemetery’s layout and organization.

## Limitations

- Field-collected points may contain minor positional inaccuracies
- Historical records are incomplete and sometimes outdated
- Manual digitization is time-intensive and subject to interpretation
- Automated feature detection was not viable at this scale

## Final Thoughts

This project showed the value of combining fieldwork, historical research, and GIS to build datasets that don’t already exist in a usable form.

It also reinforced that not all spatial problems can be solved through automation—sometimes manual work is necessary to achieve accuracy.

As I continue expanding this dataset, the goal is to create a more complete and searchable spatial record of the cemetery.


In the meantime, enjoy a 1844 drawing of Union Cemetery that was given to me by Thomas Balch Library in Leesburg, VA. 
<img width="550" height="373" alt="image" src="https://github.com/user-attachments/assets/8bbef644-b217-44a0-9e5a-fe4b7fb98bbd" />

<img width="559" height="383" alt="image" src="https://github.com/user-attachments/assets/d571e525-088f-4473-bf06-573428435c21" />


Book Sources:
Frain, Elizabeth R. Union Cemetery: Leesburg, Loudoun County, Virginia. Plats A&B 1784-1995. Willow Bend Books, 1995.
Frain, Elizabeth R. Union Cemetery: Leesburg, Loudoun County, Virginia. The Later Plats 1880-1995. Willow Bend Books, 1997.



