# creativeworks
Contains application called awesomenowcreativeworks
Digital twin -> A digital twin is a virtual model designed to accurately reflect a physical
object.
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

awesomenowcreativeworks -> Creates a digital twin of a CI based on relationships available
for that CI in CMDB.
It creates a .gml file that can be viewed in yworks yEd Graph Editor a yFiles Graph
Visualization Library.

Design notes :
awesomenowcreative works calls ServiceNow relationship API to get all relationships for a CI.
It converts that data into a .gml file which can be fed into a graph editor to visualize it.

Setup needed: 
Create a local user with role as itil or cmdb manager. This is needed only in dev or a lowest nonprod.
Same credentials need to be updated in the basic auth credentials record.
https://<instance_name>.service-now.com/basic_auth_credentials.do?sys_id=fc05b0ee07dde950b965f7208c1ed0c1
Install updateset = varanutil_GetRelationshipsForAGivenCIUpToAGivenLevel_v2.0 from github or share links below.
Download and install graph editor
https://www.yworks.com/products/yed/download


Steps to create digital twin
Create a new file or update existing file record.
Search for CI against which a digital twin needs to be created.
Save the record.
Click on create digital twin.
Refresh the form after 2 to 3 mins, a new attachment will be available.
Download the attachment and view the file in graph editor.
If local installation of graph editor is not available upload the file to
https://www.yworks.com/yed-live/ and view it on web.

Benefits :
Take snapshot of CI demographic at regular intervals.
Use to simiulate and analyze CI state in order to bring in any optimization or efficiency.

Video demo :

ServiceNow share: 

 GitHub: https://github.com/anilvaranasi/creativeworks.git
