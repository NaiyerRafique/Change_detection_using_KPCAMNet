# Change_detection_using_KPCAMNet
Change detection is the process of recognizing changes in the state of an object of focus between two time periods. This can be used to determine how certain processes are carried out in nature and what kind of anomalies can be detected. It has applications ranging from the medical field e.g. observing changes in the brain, to GIS e.g. observing changes in land areas. Change detection is of vital significance in remote sensing while observing various aerial photographs and satellite imagery. The basic premise in using remote sensing data for change detection is that changes in land cover must result in changes in radiance values. This is executed by comparing a set of images from different time periods and a digital nature of such images make them ideal for machine learning analysis. As the vast geography of earth contains various processes, change detection can have various applications like observing shifting agriculture, change in snowfall and glaciers, drought monitoring, deforestation, natural disasters, growth of concrete structures, etc. We can observe monthly, seasonal, yearly, and decadal changes to such processes and look for various anomalies

# KPCAMNet
It is a novel unsupervised change detection method that is used to extract features from very high resolution multi-temporal images through Kernel Principal Component Analysis (KPCA). This extraction of features is followed by a deep Siamese mapping network to create a pixel-wise difference map. This map is then further mapped to polar coordinates and passed through a clustering algorithm or simple thresholding operation depending on whether we require multiclass or binary class change detection.

## KPCA
![image](https://user-images.githubusercontent.com/74795452/196057043-fd936a70-b91f-44fb-bb28-f205f8b9bdac.png)
Source: https://scikit-learn.org

![image](https://user-images.githubusercontent.com/74795452/196057480-535e0e59-ef48-4eda-81f9-160063a95886.png)
Overview of the CD architecture based on the proposed KPCA-MNet 

# Dataset
Sentinel 2 satellites were launched as a part of the Copernicus program in 2015 and 2017. It specifically delivers optical imagery at a spatial resolution of 10 m to 60 m. It covers 15 spectral bands ranging from 443 to 2190 nm with a swath of 290 Km. It includes 12 bands for multispectral observations and 3 quality assurance bands. In this lab, the unannotated raster data has been acquired for the Rheinland-Pfalz region of Germany. Each image was represented as a GeoTIFF file.

The multispectral observations range from B01 to B12 with the exclusion of the B10 as it is used for water vapor and does not include surface information. The quality assurance bands consist of two true- color images at resolutions of 10 m, 20 m and 60 m and a scene classification layer (SCL). The SCL algorithm distinguishes between cloud, snow, cloud shadow, vegetation, bare soil, and water. All bands are available for each month for two years resulting in multispectral data for a total of 24 months ranging from January 2018 to December 2019. The images are unannotated therefore making it necessary to apply an unsupervised change detection method and analyze the results qualitatively. The details of the dataset used in this lab rotation have been provided in the following table:

![Screenshot (263)](https://user-images.githubusercontent.com/74795452/196057648-9d2b43ac-a7b6-4199-8b13-2923eea02cd7.png)

# Results and observations for different indices
![Screenshot (268)](https://user-images.githubusercontent.com/74795452/196057798-0353ec28-e862-49bc-9f9e-1465ea1df5a4.png)
![Screenshot (268)](https://user-images.githubusercontent.com/74795452/196057852-b7688f8f-cfb8-4705-9cee-84cda815ea1c.png)
![Screenshot (268)](https://user-images.githubusercontent.com/74795452/196057899-81231f52-4edb-4a14-84f9-c629167aa0bc.png)
![Screenshot (268)](https://user-images.githubusercontent.com/74795452/196057938-7865f7e6-71d2-4c55-a8c3-d191d4945ba6.png)
![Screenshot (268)](https://user-images.githubusercontent.com/74795452/196057970-5631e899-a85c-469c-8330-3f9ecd30d7e5.png)

# Citation
Wu, C., Chen, H., Du, B. and Zhang, L., 2021. Unsupervised change detection in multitemporal VHR images based on deep kernel PCA convolutional mapping network. IEEE Transactions on Cybernetics.

 
