# SmartFileSensor_Setup
Checks the source folder for eligible files and move them to target folder. Eligible files are the files that contain in their names a keyword that exists in keywords setup of the app configuration. The non eligible files(those for whom there is no keyword defined) with be moved under TargetFolder/_NON-ELIGIBLE-FILES_ folder.

This setup will involve the usage of three(3) different containers under Docker-Compose infrastructure. These containers are described as following:
1. The Database container which will maintain all the configuration information
2. The File Scanner Configiuration API
* Current release v1.0.0

3. The File Scanner API

* Current release v1.0.0

<p>
<details><summary>How to update the container on a host machine</summary>

<p>

1. Before updating the container you must download the following file depending on your OS:

  >* [SmartFS-Containers-WinSetup.yml for Windows OS](https://github.com/kparginos/SmartFileSensor_Setup/blob/main/SmartFC-Containers-WinSetup.yml)
  
</p>

<p>

2. Update the bindings in the scanner container with the correct folder names

3. To update to the latest version you need to do the following:

* For the Windows Host, go to the folder where the .yml file is located and run the following command:

```
docker-compose -f SmartFC-Containers-WinSetup.yml pull
```

Once finished, run the following to update the containers:

```
docker-compose -f SmartFC-Containers-WinSetup.yml up -d
```


</p>

</details>
