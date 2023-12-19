# city-scapes-script
Download City Scapes Dataset directly using this script. This makes it easier when deploying on server.  

## Getting Started
In order to use the City Scapes dataset, you need to create an account in their website (https://www.cityscapes-dataset.com/). You need to login to download the data. This makes it difficult to download the data directly on your server. You can use the script provided here to directly download the data. 
<br /> 

![dataset](https://github.com/cemsaz/city-scapes-script/blob/master/readmefiles/dataset-image.png)

## The Script
In the first command, put your username and password. This will login with your credentials and keep the associated cookie.

```
wget --keep-session-cookies --save-cookies=cookies.txt --post-data 'username=myusername&password=mypassword&submit=Login' https://www.cityscapes-dataset.com/login/
```

In the second command, you need to provide the packageID paramater. 

```
wget --load-cookies cookies.txt --content-disposition https://www.cityscapes-dataset.com/file-handling/?packageID=1
```

packageID=1 will download the file gtFine_trainvaltest.zip <br /> 
You can change it to download another package. packageIDs map like this: <br /> <br />
1: gtFine_trainvaltest.zip (241MB) <br /> 
2: gtCoarse.zip (1.3GB) <br /> 
3: leftImg8bit_trainvaltest.zip (11GB) <br /> 
4: leftImg8bit_trainextra.zip (44GB) <br /> 
5: rightImg8bit_trainvaltest.zip <br /> 
6: rightImg8bit_trainextra.zip <br /> 
7: disparity_trainvaltest.zip <br /> 
8: camera_trainvaltest.zip (2MB) <br /> 
9: camera_trainextra.zip (8MB) <br /> 
10: vehicle_trainvaltest.zip (2MB) <br /> 
11: vehicle_trainextra.zip (7MB) <br /> 
12: leftImg8bit_demoVideo.zip (6.6GB) <br /> 
13: all_demoVideo.zip <br /> 
14: leftImg8bit_sequence_trainvaltest.zip <br /> 
15: rightImg8bit_sequence_trainvaltest.zip <br /> 
16: leftImg16bit_trainvaltest.zip <br /> 
17: leftImg16bit_trainextra.zip <br /> 
18: ‘rightImg16bit_trainvaltest.zip <br /> 
19: rightImg16bit_trainextra.zip <br /> 
20: vehicle_sequence.zip <br /> 
21: timestamp_sequence.zip <br /> 
22: disparity_trainextra.zip <br /> 
23: leftImg8bit_allFrames_frankfurt.zip <br /> 
24: timestamp_allFrames_frankfurt.zip <br /> 
25: vehicle_allFrames_frankfurt.zip <br /> 
26: disparity_sequence_trainvaltest.zip <br /> 
27: rightImg8bit_allFrames_frankfurt.zip <br /> 
28: gtBbox_cityPersons_trainval.zip <br /> 
29: leftImg8bit_trainvaltest_foggy.zip <br /> 
30: leftImg8bit_trainextra_foggy.zip <br /> 
31: leftImg8bit_trainval_foggyDBF.zip <br /> 
32: leftImg8bit_blurred.zip <br /> 
33: leftImg8bit_trainval_rain.zip <br /> 
34: gtBbox3d_trainvaltest.zip <br /> 
35: gtFinePanopticParts_trainval.zip <br /> 
<br />
