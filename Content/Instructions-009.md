
### Reseting nginx to a terminal connection

1. [] From the Lab Profile page scroll down nd click the **nginx:1.20.2** Container link
1. [] Edit the container image and make the following changes:
    - In the Command dialog box enter ++bash++
    - Remove **80** from the exposed ports dialog box
!IMAGE[f3cgjv12.jpg](images/f3cgjv12.jpg)
1. [] Save the Container Image
1. [] Click the link to go back the the Lab Profile **@lab.Variable(initials): LP - @lab.Variable(initials) - nginx:1.20.2**
1. [] Launch the Lab Profile - Notice this time you are at a bash shell.

===

### Modifying the Container

>You will replace the default web site with a custom website and configure the Container to start the web server automatically.

1. [] To download the Website use the following command: ++curl -O https://ldwstorage.blob.core.windows.net/feb22/zoo.tar++ this will take upto 20 seconds.
!IMAGE[5tbzk8rw.jpg](images/5tbzk8rw.jpg)

1. [] Extract the website to the www root folder: ++tar -xvf zoo.tar -C /usr/share/nginx/html++
!IMAGE[crrh5kh4.jpg](images/crrh5kh4.jpg)

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
!IMAGE[ql7ikwwr.jpg](images/ql7ikwwr.jpg)
1. [] Cick the link to open the New Container Image
1. [] Edit the Container Image and change the following settings:
    - In the Command dialog box empty the contents
    - In the Exposed ports box type **80**
    - Ensure the Display list box has **Web** selected
!IMAGE[0ddjy3w6.jpg](images/0ddjy3w6.jpg)
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
!IMAGE[1eomaf6o.jpg](image/1eomaf6o.jpg)

1. [] Save the Lab Profile
1. [] Launch the Lab Profile - When the Lab Client loads the The browser should show the Zoo Website:
!IMAGE[p5phtt6e.jpg](images/p5phtt6e.jpg)

>[!KNOWLEDGE] This could be a web application that you wish to educate your users on and loads faster and potentially costs less than traditonal VM solutions.  Some Examples could be Ethical Web Hacking (Dam Vulnerable Web App), Programing by using Visual Studio Code in a browser or Wordpress.

- Let the instructor kow you have finished.
