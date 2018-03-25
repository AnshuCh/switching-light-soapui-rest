# switching-light-soapui-rest

Requirement: To run this project, you need SoapUI

Note: Below, I have explained how I have created this project. You just need to ‘Import Project’ in which you need to open the attached xml file which will load the project, and then you can run and verify the results.

1.	In SoapUI, open File > New Rest Project.

In URI, enter given URL: https://qa-challenges-lightbulb.atlassian.io , and click OK.

2.	A blank resource ([]) will be created with ‘Request 1’. Open ‘Request 1’ under this. You will see that ‘Method’ is selected to ‘GET’ and ‘Endpoint’ is selected to ‘ https://qa-challenges-lightbulb.atlassian.io ‘. Enter ‘Resource’ as ‘/api/allmethods’ and click to submit request.

Verify that xml content in <data> tag appears correctly. Here, if you go to browser and refresh the URL, you will see the current status of light.

You can rename your method name and Request name in the project hierarchy in Navigator pane. Here, I have renamed the method name to ‘GET’ method.

3.	Create a new resource ‘api/allmethods/off’. Verify that its request has Method as ‘GET’ (by default), Endpoint as ‘ https://qa-challenges-lightbulb.atlassian.io ‘ and Resource as ‘api/allmethods/off’. Create a new Parameter with Name as userid and value as ‘dd8e472e-302d-bc83-3c0a-f9e67966dfc5’ (If you will run the given URL in browser, URL will provide you specific userid which you can then use here in your API). Here also, I have renamed the method name to ‘GET’ method in projects hierarchy in Navigator pane.

Submit request.

Verify that JSON tab shows the response. Here, if you go to browser and refresh the URL, you will see that light has been turned off.

4.	Create a new resource ‘api/allmethods/off’. Verify that its request has Method as ‘GET’ (by default), Endpoint as ‘ https://qa-challenges-lightbulb.atlassian.io ‘ and Resource as ‘api/allmethods/off’. Change the Method to ‘POST’, and create a new Parameter with Name as userid and value as ‘dd8e472e-302d-bc83-3c0a-f9e67966dfc5’ (If you will run the given URL in browser, URL will provide you specific userid which you can then use here in your API). Here also, I have renamed Method Name in projects hierarchy in Navigator pane as ‘Post’.

Select ‘Media Type’ as ‘application/json’, and below that, in the request area, type:
{ “power”: 20 }
and submit request.

Verify that JSON tab shows the response. Here, if you go to browser and refresh the URL, you will see that light has been turned off.

5.	Create a new resource ‘api/allmethods/on’. Verify that its request has Method as ‘GET’ (by default), Endpoint as ‘ https://qa-challenges-lightbulb.atlassian.io ‘ and Resource as ‘api/allmethods/on’. Change the Method to ‘POST’, and create a new Parameter with Name as userid and value as ‘dd8e472e-302d-bc83-3c0a-f9e67966dfc5’ (If you will run the given URL in browser, URL will provide you specific userid which you can then use here in your API). Here also, I have renamed Method Name in projects hierarchy in Navigator pane as ‘Post’, and also renamed request xml to ‘Default Power’.

Select ‘Media Type’ as ‘application/json’ and submit request.

Verify that JSON tab shows the response. Here, if you go to browser and refresh the URL, you will see that FULL light has been turned on.

6.	Create a new ‘POST’ method under resource ‘api/allmethods/on’. While creating that method, give it a relevant name (I have given name as ‘Post’), select HTTP Method as ‘POST’, add new ‘userid’ parameter as done above, and click OK.

Verify that in this new Request, Method is ‘POST’, Endpoint is ‘ https://qa-challenges-lightbulb.atlassian.io ‘ , Resource is ‘api/allmethods/on’ and Parameters contains ‘?userid=dd8e472e-302d-bc83-3c0a-f9e67966dfc5’. Select Media Type as ‘application/json’ and below that, in the request area, type
{ “power”: 20 }
Now, submit the request.

Verify that JSON tab shows the response. Here, if you go to browser and refresh the URL, you will see DIM light.
