# creativeworks
**Deployment instructions**

Download attached file : ACW-SubFlow_v1.0 this is an updateset
Retrieve this updateset.
Preview and commit it.

Download attached file: varanutil_GetRelationshipsForAGivenCIUpToAGivenLevel_v2.0 this is an updateset
Retrieve this updateset.
Preview and commit it.

**Create a local user** 
Create a local user with role as itil or cmdb manager. This is needed only in dev or a lowest nonprod.
Same credentials need to be updated in the basic auth credentials record.
https://<instance_name>.service-now.com/basic_auth_credentials.do?sys_id=fc05b0ee07dde950b965f7208c1ed0c1

**Install app from github repo.**
1. Import scoped app via studio

**optional step**
Download and install graph editor, this is needed to see the output.
https://www.yworks.com/products/yed/download

**What is creative works**
Creative works is a servicenow scoped app that creates digital twin for a given scoped app or a CI (configuration item). It reates a digital twin of a CI based on relationships available for that CI in CMDB. It creates a .gml file that can be viewed in yworks yEd Graph Editor a yFiles Graph Visualization Library.

**Digital twin**
What is a digital twin ?
 A digital twin is a virtual model designed to accurately reflect a physical object.
References:
https://www.ibm.com/topics/what-is-a-digital-twin -> Turbine and a many other types
https://www.servicenow.com/workflow/it-transformation/how-digital-twins-help-mitigate-supply-chain-risk.html
 -> Manufacturing
https://www.servicenow.com/workflow/it-transformation/bring-your-digital-twin-to-work/
 -> telco
https://www.mathworks.com/videos/what-is-a-digital-twin-1633951326406.html
 -> OT (Pump)
https://www.servicenow.com/workflow/employee-engagement/the-case-for-creating-an-employee-digital-twin/
 -> HR

**Design notes**
awesomenowcreative works performs two functions
1. Create digital twin for a CI relationship as part of which calls ServiceNow relationship API to get all relationships for a CI.
It converts that data into a .gml file which can be fed into a graph editor to visualize it.


**Steps to create digital twin**
Create a new file or update existing file record.
Search for CI against which a digital twin needs to be created.
Save the record.
Click on create digital twin.
Refresh the form after 2 to 3 mins, a new attachment will be available.
Download the attachment and view the file in graph editor.
If local installation of graph editor is not available upload the file to
https://www.yworks.com/yed-live/ and view it on web.

**Benefits**
Take snapshot of CI demographic at regular intervals.
Use to simiulate and analyze CI state in order to bring in any optimization or efficiency.

Video demo :https://youtu.be/n9OlxP-J0vw
ServiceNow share: https://developer.servicenow.com/connect.do#!/share/contents/3287388_awesomenow_creativeworks_create_a_digital_twin_in_graphml_format?t=PRODUCT_DETAILS
GitHub: https://github.com/anilvaranasi/creativeworks.git

**Example digital twin for this scoped app**
   ![image](https://github.com/anilvaranasi/creativeworks/assets/29941323/a0be09e1-b261-4462-8bde-9b845b489502)

