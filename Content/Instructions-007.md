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

!IMAGE[rlibjdkb.jpg](images/rlibjdkb.jpg)

---

**Containers page**

1. [] **+ Add Container Image**
1. [] Search for ++nginx:1.20.2++ and select the one with your initials in the description field and press **OK**

!IMAGE[d40718lo.jpg](images/d40718lo.jpg)

3. [] Ensure the **Network 1** box is ticked.

!IMAGE[by6r3yt3.jpg](images/by6r3yt3.jpg)

4. [] Click Save to save the Lab Profile

Press **Next** to continue
