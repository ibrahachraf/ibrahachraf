
# Setting up Logging for cluster


Setting up logging for a Kubernetes Cluster using Rancher V2.5 logging .



## Features

* EFK stack :
  * Elasticsearch
  * FluenBit / Fluentd
  * Kibana




## Requirements : 
* Kubernetes Cluster 
* Elasticsearch and Kibana 
* Rancher : https://Ip-machine:port


## Setting up the environment 

### 1 - Installing Elasticsearch


~~~~
  1 - In the Rancher UI, go to the cluster where you want to install logging and click Cluster Explorer.
  2 - Click Apps.
  3 - Click the elasticsearch app.
  4 - In the elasticsearch configuration modify :
     * replicas 3 
     * minimaster nodes 2 
  5 - Scroll to the bottom of the Helm chart README and click Install.
~~~~

### 1 - Installing Kiabana

~~~~
  1 - In the Rancher UI, go to the cluster where you want to install logging and click Cluster Explorer.
  2 - Click Apps.
  3 - Click the elasticsearch app.
  4 - Scroll to the bottom of the Helm chart README and click Install.
~~~~



### 3 - Enabling Logging for Rancher Managed Clusters 

~~~~
  1 - In the Rancher UI, go to the cluster where you want to install logging and click Cluster Explorer.
  2 - Click Apps.
  3 - Click the logging app.
  4 - Scroll to the bottom of the Helm chart README and click Install.
~~~~

## Configuring the Logging Application
To configure the logging application, go to the Cluster Explorer in the Rancher UI. In the upper left corner, click Cluster Explorer > Logging.

### 1 - Create Cluster Output :

![Cluster Output ](https://i.ibb.co/9gG6hms/clusteroutput.png)
* Leave other configuration as default .
### 2 - Create Custerflow :

![Cluster Flow ](https://i.ibb.co/J2CmG8C/clusterflow.png)
* Leave other configuration as default .

### 3 - Configure Cluster Output in Rancher Cluster manager :
* Select tools --> logging
  * Choose Elasticsearch
  * Endpoint :
  * Index Pattern Prefix : <index name>
  * Click test to ensure that the configuration is ok .
  * Click save 

## Configuring Kibana Dashboard  

Go to : https://kibana.platosystem.io/

1 - add the "_time" metafield : 
~~~~
  * Under Management Click Stack Management
  * Under Kibana Click Avanced settings
  * Scroll down to metafields and add _time
~~~~
  ![Kibana metafield](https://i.ibb.co/vw6Y0gM/metafield.png)
2 - Create index Pattern :
~~~~
  * Under Management Click Stack Management
  * Under Kibana Click Index patterns
  * Click Create index pattern and choose the index written in the cluster manager previously
  * choose _time time field
  * Click Create Index Pattern
~~~~
Then Go to discover under Analytics , there you can see the logs generated .

![Discover](https://i.ibb.co/DR7H7KP/discover.png)

### Kiabana Dashboard : 
![Dashboard](https://i.ibb.co/wLDXjTQ/dashboard.png)
ter


Setting up logging for a Kubernetes Cluster using Rancher V2.5 logging .



## Features

* EFK stack :
  * Elasticsearch
  * FluenBit / Fluentd
  * Kibana




## Requirements : 
* Kubernetes Cluster 
* Elasticsearch and Kibana 
* Rancher : https://Ip-machine:port


## Setting up the environment 

### 1 - Installing Elasticsearch


~~~~
  1 - In the Rancher UI, go to the cluster where you want to install logging and click Cluster Explorer.
  2 - Click Apps.
  3 - Click the elasticsearch app.
  4 - In the elasticsearch configuration modify :
     * replicas 3 
     * minimaster nodes 2 
  5 - Scroll to the bottom of the Helm chart README and click Install.
~~~~

### 1 - Installing Kiabana

~~~~
  1 - In the Rancher UI, go to the cluster where you want to install logging and click Cluster Explorer.
  2 - Click Apps.
  3 - Click the elasticsearch app.
  4 - Scroll to the bottom of the Helm chart README and click Install.
~~~~



### 3 - Enabling Logging for Rancher Managed Clusters 

~~~~
  1 - In the Rancher UI, go to the cluster where you want to install logging and click Cluster Explorer.
  2 - Click Apps.
  3 - Click the logging app.
  4 - Scroll to the bottom of the Helm chart README and click Install.
~~~~

## Configuring the Logging Application
To configure the logging application, go to the Cluster Explorer in the Rancher UI. In the upper left corner, click Cluster Explorer > Logging.

### 1 - Create Cluster Output :

![Cluster Output ](https://i.ibb.co/9gG6hms/clusteroutput.png)
* Leave other configuration as default .
### 2 - Create Custerflow :

![Cluster Flow ](https://i.ibb.co/J2CmG8C/clusterflow.png)
* Leave other configuration as default .

### 3 - Configure Cluster Output in Rancher Cluster manager :
* Select tools --> logging
  * Choose Elasticsearch
  * Endpoint :
  * Index Pattern Prefix : <index name>
  * Click test to ensure that the configuration is ok .
  * Click save 

## Configuring Kibana Dashboard  

Go to : https://kibana.platosystem.io/

1 - add the "_time" metafield : 
~~~~
  * Under Management Click Stack Management
  * Under Kibana Click Avanced settings
  * Scroll down to metafields and add _time
~~~~
  ![Kibana metafield](https://i.ibb.co/vw6Y0gM/metafield.png)
2 - Create index Pattern :
~~~~
  * Under Management Click Stack Management
  * Under Kibana Click Index patterns
  * Click Create index pattern and choose the index written in the cluster manager previously
  * choose _time time field
  * Click Create Index Pattern
~~~~
Then Go to discover under Analytics , there you can see the logs generated .

![Discover](https://i.ibb.co/DR7H7KP/discover.png)

### Kiabana Dashboard : 
![Dashboard](https://i.ibb.co/wLDXjTQ/dashboard.png)




 


