#Getting JMeter up and running
###Hoetkeys

Command + r = run  
Command + e = clear  
Command + t = toggle between active/deactivate sampler 

###How to record scripts

- If you need to record SSH then the Jmeter properties need to specify that you are recording SSH

- In the Jmeter GUI, open templates and choose recording template.  Check the HTTP recorder for the port its listening on, usually set to 8888

- Open firefox then -> properties -> network -> connection settings

- Choose manual proxy settings and choose HTTP and SSH using __localhost__ and port ftom HTTP recorder
- Start recording in Jmeter Http recorder, your transactions will start tracing browsing activity
- It's a good idea to start naming the transaction controllers that are created something user friendly so you can go back and identify what parts of the site you were accessing afterwards.  
- Stop recording and look into any of the transactions to see where to swap things like username, password, environment variables, etc.

###Run Headless
`./jmeter -n -t test.jmx -l testoutputifyouwantit.jtl` (or .csv)

###variable swap for hostname
- Can use the command line to enter a variable by typing 
`-JTestIP=10.0.0.1`
- Then in the project whereever you need it you can use this to access it
`${__P(TestIP)}`

###Troubleshoot
- When using threads and loops you have to enable the scheduler and set an amount of time to run =< the time it takes to run the test.  I let this be an arbitrarily long amount of time
- threads / ramp-up period (secs) = time after which each thread will start executing.  ie 2 threads / 60 ramp-up = 1 thread every 30 secs

