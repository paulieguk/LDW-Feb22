# Welcome to the Lab Developer Workshop - February 2022
## Introduction to Containers on LOD

### Before you start

Please enter your initials here @lab.TextBox(initials)

Press **Next** to continue

---
===

## Lab - 1 Building your first container lab profile

Press **Next** to continue

---
===

### Investigating the Docker Hub

---
1. [] Click the link to visit the [Docker Hub](https://hub.docker.com/ "Optional link title")  
1. [] Using the search box !IMAGE[Docker Hub Search](images/6xvbrzqv.jpg) and search for applications or operating systems that get used in you company.
@lab.Activity(Question1)
1. [] If so list one or two here: @lab.TextBox(apps)
1. [] In the Search box type **ubuntu** and select the Ubuntu Official image.

!IMAGE[Docker Hub Search](images/ak02lpo7.jpg)

1. [] Scroll down the details page and notice he information provided.  Especially focues on the version list, we will use this later.

### Review Container Options

1. [] In LabOnDemand navigate to the Admin Page
1. [] Notice the options in the Containers box, they should look like below

!IMAGE[4rdrj25l.jpg](4rdrj25l.jpg)

@lab.Activity(Question2)

---

1. [] In the Containers tile, select **Container Registries** and press **Search**  
1. [] Notice the **ldw-feb2022** Registry.  Click **Edit**
    - Notice this Registry is hosted on the Docker Hub
    - It supports **Private** stores which is defined by the need for credentials
1. [] Review the [Skillable Help](https://docs.learnondemandsystems.com/lod/container-registries.md?appid=lod), focusing on the following:
    - Address
    - Allow Push
    - Admin User Account
1. [] Click **Cancel** (bottom left) or **Details** (top right).  We will use a prebuilt Registry

Press **Next** to continue

---
===

### Creating Your First Container

---
1. [] From the Admin page select **Container Images** from the Containers tile
1. [] Click **+ Create Container Images** from the top right corner
!IMAGE[tewgbvaf.jpg](tewgbvaf.jpg)
1. [] Complete the form as follows:

| Field | Value |
|:---------|:---------|
| Name   | ++ubuntu:latest++   |
| Description  | ++@lab.Variable(initials) - Ubuntu++   |
| Organization | ++LDW-Feb22++ |
| Registry | ++Docker Hub++ |
| Size | **Nano** |

1. [] Click **Save**

Press **Next** to continue

---
===

### Create a Lab Profile to host the Container image

---

1. [] From the Admin page select **Create Lab Profile** from the Lab Profile tile
1. [] From the top right select **+ Create Custom Environment**
1. [] Complete the Lab Profile as follows:

**Basic page** 

Complete the following fields:

| Field Name | Value |
|:---------|:---------|
| Number | ++@lab.Variable(initials)++ |
| Name   | ++LP - @lab.Variable(initials) - ubuntu Docker++   |
| Series   | ++LDW-FEB22++ |
| Organization | ++LDW-Feb22++ |
| Virtualization Platform | **Docker** |

---

**Networks page**

1. [] Add a network all the defaults should be correct:

!IMAGE[rlibjdkb.jpg](rlibjdkb.jpg)

---

**Containers page**

1. [] **+ Add Container Image**
1. [] Search for ++ubuntu:latest++ and select the one with **@lab.Variable(initials) - ubuntu docker** in the description field and press **OK**

!IMAGE[kg00tr4s.jpg](kg00tr4s.jpg)

3. [] Ensure the **Network 1** box is ticked.

!IMAGE[8xey4fz6.jpg](8xey4fz6.jpg)

4. [] Click Save to save the Lab Profile

Press **Next** to continue

---
===

### Testing the Container

1. [] Click Launch to launch the **@lab.Variable(initials): LP - @lab.Variable(initials) - ubuntu Docker** Lab Profile

>[!Knowledge] Notice how quickly the container starts compared to a traditional VM.

1. [] At the bash prompt type ++cat /etc/os-release++  This will show the Ubuntu version.  Record the version number below:
@lab.TextBox(ubuntulatest)

1. [] End the Lab
1. [] From the Lab Profile page open the scroll down and click on the Container **ubuntu:latest**
1. [] Edit the Comtainer image
1. [] Change the Name from **ubuntu:latest** to ++ubuntu:16.04++

>[!Tip] This will change the container version to the older 16.04 version which was released in April 2016.

6. [] Click Save and launch the lab again (link to the Lab Profile is on the Container image page)
1. [] At the bash prompt type ++cat /etc/os-release++  This will show the Ubuntu version.
6. [] Compare this version number to the number before.  The previous version was @lab.Variable(ubuntulatest)
6. [] End the **LP - @lab.Variable(initials) - Ubuntu Docker** lab and let the instructor know you have finished Lab 1.

Press **Next** to continue

---
===

## Lab - 2 Using a Web connection to a Container

Press **Next** to continue

---

===

### Investigating a Web connection container image

The previous lab you created a container and connected to the container using a bash shell.  This time you will create a new container image this time connecting via a Web connection. nginx is a light weight web server and you will be using a container that has that contains that WebServer

1. [] From the Admin page select **Container Images** from the Containers tile
1. [] Click **+ Create Container Images** from the top right corner

!IMAGE[tewgbvaf.jpg](tewgbvaf.jpg)

1. [] Complete the form as follows and save the Container Image:

| Field | Value |
|:---------|:---------|
| Name   | ++nginx:1.20.2++   |
| Description  | ++@lab.Variable(initials) - nginx++    |
| Organization | ++LDW-Feb22++ |
| Registry | ++Docker Hub++ - Default Organization |
| Command | Clear the contents |
| Exposed Ports | 80 |
| Display | Web |

Press **Next** to continue

---

===

### Create a Lab Profile to host the web Container image

---

1. [] From the Admin page create a custom environment Lab Profile
1. [] Complete the Lab Profile as follows:

**Basic page** 

Complete the following fields:

| Field Name | Value |
|:---------|:---------|
| Number | ++@lab.Variable(initials)++ |
| Name   | ++LP - @lab.Variable(initials) - nginx:1.20.2++   |
| Series   | ++LDW-FEB22++ |
| Organization | ++LDW-Feb22++ |
| Virtualization Platform | **Docker** |

---

**Networks page**

1. [] Add a network all the defaults should be correct:

!IMAGE[rlibjdkb.jpg](rlibjdkb.jpg)

---

**Containers page**

1. [] **+ Add Container Image**
1. [] Search for ++nginx:1.20.2++ and select the one with your initials in the description field and press **OK**

!IMAGE[d40718lo.jpg](d40718lo.jpg)

3. [] Ensure the **Network 1** box is ticked.

!IMAGE[by6r3yt3.jpg](by6r3yt3.jpg)

4. [] Click Save to save the Lab Profile

Press **Next** to continue

---

===

### Testing the nginx Web Container

1. [] Click Launch to launch the **LP - @lab.Variable(initials): LP - @lab.Variable(initials) - nginx:1.20.2** Lab Profile
1. [] Notice this time you are connected to the default web page in the container
1. [] End the **LP - @lab.Variable(initials): LP - @lab.Variable(initials) - nginx:1.20.2** lab.
1. [] Let the instructor know you have finished Lab 2.

Press **Next** to continue

---
===

## Lab - 3 Modifying/Updating a Container Image

---
===

### Reseting nginx to a terminal connection

1. [] From the Lab Profile page scroll down nd click the **nginx:1.20.2** Container link
1. [] Edit the container image and make the following changes:
    - In the Command dialog box enter ++bash++
    - Remove **80** from the exposed ports dialog box
!IMAGE[f3cgjv12.jpg](f3cgjv12.jpg)
1. [] Save the Container Image
1. [] Click the link to go back the the Lab Profile **@lab.Variable(initials): LP - @lab.Variable(initials) - nginx:1.20.2**
1. [] Launch the Lab Profile - Notice this time you are at a bash shell.

===

### Modifying the Container

>You will replace the default web site with a custom website and configure the Container to start the web server automatically.

1. [] To download the Website use the following command: ++curl -O https://ldwstorage.blob.core.windows.net/feb22/zoo.tar++ this will take upto 20 seconds.
!IMAGE[5tbzk8rw.jpg](5tbzk8rw.jpg)

1. [] Extract the website to the www root folder: ++tar -xvf zoo.tar -C /usr/share/nginx/html++
!IMAGE[crrh5kh4.jpg](crrh5kh4.jpg)

### Saving the Container

1. [] From the Burger menu select **Save -> Commit changes and update this Lab Profile**
1. [] Complete the form as follows:
    - Note: Installed Zoo Website
    - Registry: ldw-Feb2022
    - Image Name: paulie/@lab.Variable(initials)-nginx:1.0.0
1. [] Click OK

>The container should save within a minute or two.  Having updated the container you will use a Life Cycle Action to ensure that the Web Server always starts, this could also be done by editing the container configuration.  The reason for using an LCA is to build on the learning from Decembers LDW.

4. [] Once the save is complete Click OK and end the Lab **@lab.Variable(initials): LP - @lab.Variable(initials) - nginx:1.20.2**

---
===

### Modifying the Container Image Profile

>In this section the Container image needs to be reconfigured for Web display and the LCA needs to be created.

1. [] Switch back to the Lab Profile Tab (**@lab.Variable(initials): LP - @lab.Variable(initials) - nginx:1.20.2**).  Refresh the page (by right clicking the page and selecting refresh).  Notice the Container Image name has changed to the new Image you just created.  **paulie/@lab.Variable(initials)-nginx:1.0.0**
!IMAGE[ql7ikwwr.jpg](ql7ikwwr.jpg)
1. [] Cick the link to open the New Container Image
1. [] Edit the Container Image and change the following settings:
    - In the Command dialog box empty the contents
    - In the Exposed ports box type **80**
    - Ensure the Display list box has **Web** selected
!IMAGE[0ddjy3w6.jpg](0ddjy3w6.jpg)
1. [] Save the Container Image and switch back to the Lab Profile **@lab.Variable(initials): LP - @lab.Variable(initials) - nginx:1.20.2** by clicking the link.

Press **Next** to continue

---
===

### Creating the Lab Profile LCA

1. [] Edit the Lab Profile.
1. [] Create a Life Cycle Action with the following settings
    - Name: +++Start Web Server+++
    - Action: Execute Script in Container
    - Event: First Displayable
    - Blocking: Selected
    - Container Image: **nginx**
    - Script: ++service nginx start &++
!IMAGE[1eomaf6o.jpg](1eomaf6o.jpg)

1. [] Save the Lab Profile
1. [] Launch the Lab Profile - When the Lab Client loads the The browser should show the Zoo Website:
!IMAGE[p5phtt6e.jpg](p5phtt6e.jpg)

>[!KNOWLEDGE] This could be a web application that you wish to educate your users on and loads faster and potentially costs less than traditonal VM solutions.  Some Examples could be Ethical Web Hacking (Dam Vulnerable Web App), Programing by using Visual Studio Code in a browser or Wordpress.

- Let the instructor kow you have finished.
