# city-scapes-script
Download City Scapes Dataset directly using this script. This makes it easier when deploying on server.  

## Getting Started
In order to use the City Scapes dataset, you need to create an account in their website (https://www.cityscapes-dataset.com/). You need to login to download the data. This makes it difficult to download the data directly on your server. You can use the script provided here to directly download the data. 
<br /> 

![dataset](https://github.com/cemsaz/city-scapes-script/blob/master/readmefiles/dataset-image.png)

<br /> 

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
You can change it download another dataset. packageIDs map like this: <br /> <br />
1 -> gtFine_trainvaltest.zip (241MB) <br />
2 -> gtCoarse.zip (1.3GB) <br />
3 -> leftImg8bit_trainvaltest.zip (11GB) <br />
4 -> leftImg8bit_trainextra.zip (44GB) <br />
8 -> camera_trainvaltest.zip (2MB) <br />
9 -> camera_trainextra.zip (8MB) <br />
10 -> vehicle_trainvaltest.zip (2MB) <br />
11 -> vehicle_trainextra.zip (7MB) <br />
12 -> leftImg8bit_demoVideo.zip (6.6GB) <br />
28 -> gtBbox_cityPersons_trainval.zip (2.2MB) <br />
<br />
