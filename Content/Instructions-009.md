1. [] From the Lab Profile page scroll down nd click the **nginx:1.20.2** Container link
1. [] Edit the container image and make the following changes:
    - In the Command dialog box enter ++bash++
    - Remove **80** from the exposed ports dialog box
!IMAGE[f3cgjv12.jpg](images/f3cgjv12.jpg)
1. [] Save the Container Image
1. [] Click the link to go back the the Lab Profile **@lab.Variable(initials): LP - @lab.Variable(initials) - nginx:1.20.2**
1. [] Launch the Lab Profile - Notice this time you are at a bash shell.

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

Press **Next** to continue
