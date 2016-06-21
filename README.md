broadleaf-starter-kit
===================

Version 1.1-34p
---------------

[![Install](https://raw.github.com/qubell-bazaar/component-skeleton/master/img/install.png)](https://express.qubell.com/applications/upload?metadataUrl=https://raw.github.com/qubell-bazaar/broadleaf-starter-kit/gce/meta.yml)

![](http://www.broadleafcommerce.com/img/broadleaf_logo_white.png)
![](http://tomcat.apache.org/images/tomcat-power.gif)
![](https://lucene.apache.org/images/solr.png)

This is example of  Broadleaf eCommerce applications with SolrCloud as a search engine   [Qubell Adaptive PaaS](http://qubell.com).

Features
--------

 - Install Broadleaf DemoSite with Admin panel  on one or more Tomcat nodes in parallel 
 - Install Haproxy as load balance for application nodes
 - Install SolrCloud with Zookeeper ensemble and point application to Zookeper hosts  
 - Scale app and down application cluster
 - Rebuild application by switching git branch
    
    
Configurations
--------------

 - Broadleaf 3.1.0 , Amazon Linux (us-east-1/ami-1ba18d72), AWS EC2 m1.small, ec2-user
 - Broadleaf 3.1.0 , CentOS 6.4 (us-east-1/ami-bf5021d6), AWS EC2 m1.small, root
 - Broadleaf 3.1.0 , Ubuntu 12.04 (us-east-1/ami-967edcff), AWS EC2 m1.small, ubuntu
 - Broadleaf 3.1.0 , Ubuntu 10.04 (us-east-1/ami-9f3906f6), AWS EC2 m1.small, ubuntu

    
- [Tomcat 6](https://github.com/qubell-bazaar/component-tomcat-dev), [MySQL 5](https://github.com/qubell-bazaar/component-mysql-dev), [HAProxy 1.4](https://github.com/qubell-bazaar/component-haproxy) [Solr 4.4](https://github.com/qubell-bazaar/component-solr-dev)
    
Pre-requisites
--------------
 - Configured Cloud Account a in chosen environment
 - Either installed Chef on target compute OR launch under root
 - All pre-requisites from the components above

<a name="how-does-it-work"></a>
### How Does this Kit Work?

Broadleaf Starter Kit has three main components:

* **Broadleaf Demo site** - The Heat Clinic eCommerce store.
* **Broadleaf admin panel** - The Administration Panel  for easy  Broadleaf catalog management.
* **Solr Cloud Search Engine** - A search engine that indexes and executes search queries from Broadleaf catalog.
   By default Broadleaf use embeded Solr support. But in our demo  we setup  a full Solr cluster - 4 nodes 2 shards with Zookeeper ensemble - 3 nodes.
   We use our fork Broadleaf DemoSite [https://github.com/qubell-bazaar/DemoSite](https://github.com/qubell-bazaar/DemoSite).It contain:
      -  preconfigured archive with solr collection files  
      -  changed sources for support mysql and solr cloud

<a name="setup"></a>
## Setup
You will need to set up the following in order to use Broadleaf Starter Kit:

* A [Qubell Adaptive PaaS](http://qubell.com) account
* An Amazon AWS account
* Access to git repository with CRS sources *(optional)*

Please refer to the steps below for getting set up.

<a name="step-by-step-setup"></a>
### Step-by-step Setup Guide
- **[Step 1. Set up and Configure an Amazon Web Services (AWS) Account](docs/step-1-amazon-setup-guide.md)**
- **[Step 2. Set up a Qubell Account](docs/step-2-qubell-setup-guide.md)**
- **[Step 3. Obtain the Broadleaf Starter Kit](docs/step-3-get-starter-kit.md)**
- **[Step 4. Launch the Application](docs/step-4-launch-guide.md)**

