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

!IMAGE[rlibjdkb.jpg](images/rlibjdkb.jpg)

---

**Containers page**

1. [] **+ Add Container Image**
1. [] Search for ++ubuntu:latest++ and select the one with **@lab.Variable(initials) - ubuntu docker** in the description field and press **OK**

!IMAGE[kg00tr4s.jpg](images/kg00tr4s.jpg)

3. [] Ensure the **Network 1** box is ticked.

!IMAGE[8xey4fz6.jpg](images/8xey4fz6.jpg)

4. [] Click Save to save the Lab Profile

Press **Next** to continue
