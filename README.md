

This is the monolithic version of this demo. 
For the micro-services version, please see the microservices branch: https://github.com/Pivotal-Field-Engineering/PCF-demo/tree/micro-services

PCF Demo
=========

1) Login to your org and space :
cf login -a api.my-unique-domain.io
When prompted please select username, password, org and space
2) Deploy application for the main directory :
cf push (name, hostname, instances, memory is specified in the manifest.yml)
You can use specific manifest for specific env. Use -f to specify specific manifest
Push the application initially with no service bound.
Notice it will alert no RabbitMQ service is bound.. the link "Stream Data" will not work either.
Now, bind a RabbitMQ service. Re-push the app.
Click "Stream Data" and see the fun start. Click on a state to detail orders going throw it.
3) Use "cf apps" to see the apps running in your env.
Additional fun: click "Kill App" and watch the application crashing.. it will show as "crashed" when you visualize events (cf events <app_name>). Health manager will automatically restart the app for you.





