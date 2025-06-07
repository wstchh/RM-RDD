# RM-RDD: A Multi-Class Road Defect Dataset Tailored for Real-World Vehicle Driving Scenarios

At present, publicly available datasets for road defect detection are relatively limited, with most providing only precise location annotations of defects, thereby failing to fully represent the real-world conditions of road surfaces. To address this limitation, some researchers have employed in-vehicle cameras, such as dashcams, for data collection, leading to the creation of publicly available datasets such as RDD2020[1] , RDD2022[2] , and N-RDD2024[3] . However, these datasets still exhibit certain shortcomings: the number of annotated defect categories is limited, the captured environments are often simplified or idealized, and there is a lack of diverse and realistic road scenarios. Moreover, in practical applications, image quality can be significantly degraded by various factors, including windshield reflections, glare from direct sunlight, and occlusions caused by the vehicle hood, which further increases the complexity of road defect detection.

With this objective, we present RM-RDD, a multi-class road defect dataset that is closely aligned with real-world vehicle driving scenarios. During the data collection process, real-time images were captured by engineering vehicles equipped with imaging sensors traveling at normal driving speeds (as illustrated in Fig. 5). The collected images cover a wide range of road types, including highways, provincial roads, and urban streets, ensuring both the diversity and reliability of the dataset. The dataset was collected from various road segments across multiple cities in China, under different temporal conditions such as morning and evening rush hours, daytime, and nighttime. It also incorporates a variety of weather conditions, including sunny, rainy, cloudy, and foggy days, as well as diverse lighting environments such as strong direct sunlight, backlighting, and low-light conditions. These factors significantly enhance the realism and complexity of the road defect detection task. Furthermore, the dataset accounts for variations in vehicle speed, camera mounting height, and installation angle, thereby improving its practical applicability. To ensure data privacy and security, sensitive information such as human faces and license plates has been anonymized using appropriate de-identification techniques.

<table frame=void>
	<tr>
    <td><center><img src="Pic/Sensor-Vehicle-1.jpg"
                     alt="Typora-Logo"
                     height="200"
            		 width="300"/></center></td>
    <td><center><img src="Pic/Sensor-Vehicle-2.jpg"
                     alt="Typora-Logo"
                     height="200"
                     width="300"/></center></td>
    <td><center><img src="Pic/Sensor-Vehicle-3.jpg"
                     alt="Typora-Logo"
                     height="200"
                     width="300"/></center></td>
    <td><center><img src="Pic/Sensor-Vehicle-4.jpg"
                     alt="Typora-Logo"
                     height="200"
                     width="300"/></center></td> 
    </tr>
</table>

​                                                                               Fig. 6. Samples from the RM-RDD datase









<table frame=void>
	<tr>
    <td><center><img src="Pic/Vehicle Deployment.png"
                     alt="Typora-Logo"
                     height="500"
            		 width="500"/></center></td>
    </tr>
</table>





<table frame=void>
	<tr>
    <td><center><img src="Pic/Vehicle-mounted Camera.jpg"
                     alt="Typora-Logo"
                     height="200"
                     width="300"/></center></td> 
    <td><center><img src="Pic/GPS.jpg"
                     alt="Typora-Logo"
                     height="200"
                     width="300"/></center></td> 
    <td><center><img src="Pic/AI Chip Equipment.jpg"
                     alt="Typora-Logo"
                     height="200"
                     width="300"/></center></td> 
    </tr>
</table>











<table frame=void>
	<tr>
    <td><center><img src="Pic/1.jpg"
                     alt="Typora-Logo"
                     height="200"
                     width="300"/></center></td>
    <td><center><img src="Pic/2.jpg"
                     alt="Typora-Logo"
                     height="200"
                     width="300"/></center></td>
    <td><center><img src="Pic/3.jpg"
                     alt="Typora-Logo"
                     height="200"
                     width="300"/></center></td>
    </tr>
    <tr>	<!--第二行-->
    <td><center><img src="Pic/4.jpg"
                     alt="Typora-Logo"
                     height="200"
                     width="300"/></center></td> 
    <td><center><img src="Pic/5.jpg"
                     alt="Typora-Logo"
                     height="200"
                     width="300"/></center></td> 
    <td><center><img src="Pic/6.jpg"
                     alt="Typora-Logo"
                     height="200"
                     width="300"/></center></td> 
    </tr>
</table>




In November 2024, we established the RM-RDD dataset. The road defect types studied in this paper include eight categories: potholes (D00),  subsidence (D01), longitudinal cracks (D02), longitudinal crack patches (D03), transverse cracks (D04), transverse crack patches (D05), alligator cracks (D06), and alligator crack patches (D07). The dataset comprises a total of **10,440** annotated images, partitioned into a **training set (8,119 images)**, a **validation set (1,000 images)**, and a **test set (1,321 images)**. Representative examples of the different road defect types are shown in Fig. 6, and the class distribution is summarized in the following table.
 
​                                                                  Category Distribution of the RM-RDD Dataset

					|    Road Damage Types     | Label | Training Set | Validation  Set | Testing Set | Total |
					| :----------------------: | :---: | :----------: | :-------------: | :---------: | :---: |
					|         Pothole          |  D00  |     1717     |       521       |     199     | 2437  |
					|        Subsidence        |  D01  |     1229     |       49        |     282     | 1560  |
					|    Longitudinal Crack    |  D02  |     2822     |       418       |     401     | 3641  |
					| Longitudinal Crack Patch |  D03  |     4144     |       473       |     843     | 5460  |
					|     Transverse Crack     |  D04  |     2478     |       315       |     328     | 3121  |
					|  Transverse Crack Patch  |  D05  |     4893     |       514       |    1005     | 6412  |
					|     Alligator Crack      |  D06  |     1177     |       175       |     129     | 1481  |
					|  Alligator Crack Patch   |  D07  |     1058     |        75       |     171     | 1304  |

​                                                                                              Category Distribution of the RM-RDD2025 Dataset

|    Road Damage Types     | Label | Training Set | Validation  Set | Testing Set | Total |
| :----------------------: | :---: | :----------: | :-------------: | :---------: | :---: |
|         Pothole          |  D00  |     1717     |       777       |     199     | 2693  |
|        Subsidence        |  D01  |     1229     |       74        |     282     | 1585  |
|    Longitudinal Crack    |  D02  |     2822     |       644       |     401     | 3867  |
| Longitudinal Crack Patch |  D03  |     4144     |       723       |     843     | 5710  |
|     Transverse Crack     |  D04  |     2478     |       446       |     328     | 3252  |
|  Transverse Crack Patch  |  D05  |     4893     |       841       |    1005     | 6739  |
|     Alligator Crack      |  D06  |     1177     |       247       |     129     | 1553  |
|  Alligator Crack Patch   |  D07  |     1058     |       101       |     171     | 1330  |

​																



## 🚀 Updates
- \[2024.11.28\] Add torch tool for parameters and flops statistics. see [run_profile.py](./rtdetrv2_pytorch/tools/run_profile.py)
- \[2025.11.28\] Add torch tool for parameters and flops statistics. see [run_profile.py](./rtdetrv2_pytorch/tools/run_profile.py)
- \[2024.11.28\] Add torch tool for parameters and flops statistics. see [run_profile.py](./rtdetrv2_pytorch/tools/run_profile.py)





## 🦄 Performance
