# Introduction and Mapping the Scientific Area

## Introduction

Our task is to build a model that locate ships in satellite images, and put an aligned bounding box segment around the ships we locate. Many images do not contain ships, and those that do, may contain multiple ships. Ships within and across images may differ in size (sometimes significantly) and be located in open sea, at docks, marinas, etc.

## Background and motivation

With the rapid growth of global shipping traffic, the maritime monitoring has become increasingly crucial. Detecting and tracking ships from space can be an important step to support the fully-automated self-driving ships and avoid accidents which can couse irreversible damages to our world.

The system has several benefits:

-**Environmental protection**: As it was mentioned earlier, it helps to avoid accidents like oil spill and also can monitor illegal fishing.  
-**Security**: The system can improve the surveillance of the ships to prevent and prepare for piracy attacks.  
-**Logistics and fleet management**: with the continuous monitoring of vessel positions supports route optimization, imporves scheduling accuracy.  


## Scientific Context

The description of the competition raises an especially interesting question: **Can you find them even in imagery with clouds of haze?** We did a research about this question. 

This problem is scientifically important because atmospheric effect such as **clouds, haze and sun reflections can partially or completely obscure ships, reducing the visibility of their shapes and texture. Detecting ships under these conditions requires both high-quality data and robust image processing techniques. 

-**Cloud masking and atmospheric correction**: algorithms that identify and remove clouded pixels, or correct the brightness distortion caused by haze.  
-**Multi-spectral and synthetic aperture radar(SAR) imagery**: SAR sensoers operate in the microwave range, which can penetrate clouds and haze, providing clear signals even during poor weather or nighttime.  
-**Data fusion**: combining optical and radar data to leverage the detailed texture of optical images with the robustness of SAR data.  
-**Deep learning-based enhancement**: using neural networks (such as GANs or transformers) to restore visibility in hazy regions or learn features invariant to cloud coverage.  

Therefore, while detecting ships in different weather conditions is quite challenging, it is possible with the right combination of data sourcing and preprocessing.

However, in the Airbus dataset only RGB optical images are available, which means that we cannot apply radar-based or multi spectral approaches. We are not be able to see through clouds with RGB images. A preprocessing technique which can be useful to reach better result is contrast enhancement, to improve visibility in low-contrast areas.

## Bibliography

Airbus. (n.d.). Earth observation imagery and data. Airbus Space Solutions. Retrieved November 5, 2025, from https://space-solutions.airbus.com/imagery/

European Union Satellite Centre (SatCen). (n.d.). SAR Course. Retrieved November 5, 2025, from https://www.satcen.europa.eu/page/sar_course_sar_

Farmonaut. (n.d.). Can satellites see through clouds? 5 insights. Retrieved November 5, 2025, from https://farmonaut.com/remote-sensing/how-satellites-see-through-clouds-5-powerful-insights

NASA Earthdata. (n.d.). Seeing Earth in a new light. Retrieved November 5, 2025, from https://www.earthdata.nasa.gov/news/feature-articles/seeing-earth-new-light

NASA Earthdata. (n.d.). Synthetic Aperture Radar (SAR). Retrieved November 5, 2025, from https://www.earthdata.nasa.gov/learn/earth-observation-data-basics/sar

NASA Earth Observatory. (n.d.). Why is that forest red and that cloud blue? How to interpret a false-color satellite image. Retrieved November 5, 2025, from https://earthobservatory.nasa.gov/features/FalseColor/page5.php

The Open University. (n.d.). Watching the weather. OpenLearn. Retrieved November 5, 2025, from https://www.open.edu/openlearn/nature-environment/environmental-studies/watching-the-weather/content-section-2.2