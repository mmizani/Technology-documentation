#Getting JMeter up and running
###Hoetkeys

Command + r = run  
Command + e = clear  
Command + t = toggle between active/deactivate sampler 

###How to record scripts

- If you need to record SSH then the Jmeter properties need to specify that you are recording SSH

- In the Jmeter GUI, open templates and choose recording template.  Check the HTTP recorder for the port its listening on, usually set to 8888

- Open firefox then -> properties -> network -> connection settings

- Choose manual proxy settings and choose HTTP and SSH using port ftom HTTP recorder
