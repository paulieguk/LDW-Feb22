The previous lab you created a container and connected to the container using a bash shell.  This time you will create a new container image this time connecting via a Web connection. nginx is a light weight web server and you will be using a container that has that contains that WebServer

1. [] From the Admin page select **Container Images** from the Containers tile
1. [] Click **+ Create Container Images** from the top right corner

!IMAGE[tewgbvaf.jpg](images/tewgbvaf.jpg)
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
