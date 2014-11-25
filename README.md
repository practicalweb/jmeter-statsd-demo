jmeter statsd demo
==================


To run this demo and test out logging to statsd from jmeter 

Get jmeter (I used 2.8) add the statsd jar file to jmeter's /lib 



```bash
git clone git@github.com:practicalweb/jmeter-statsd-demo.git
cd jmeter-statsd-demo
wget https://archive.apache.org/dist/jmeter/binaries/apache-jmeter-2.8.tgz
tar -xzf apache-jmeter-2.8.tgz
cd apache-jmeter-2.8/
cd lib/
wget https://github.com/tim-group/java-statsd-client/releases/download/v3.0.1/java-statsd-client-3.0.1.jar
cd ..
./bin/jmeter
```

With jmeter running load the statsd-demo.jmx test plan

You'll want to edit this so that the beanshell pre-processor connects to your statsd server

and the HTTP request loads the site you want to test 



