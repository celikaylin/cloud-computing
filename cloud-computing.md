# Cloud Computing

Cloud computing is out there not on premises. **Wrong** because commercial facities are off premises and actually they are not cloud and private cloud deployments on primeses (we will see next topics)

Here is the NIST defination. (You can checj NIST from [here](https://www.nist.gov/))

*Cloud computing is a model for enabling ubiquitous, convenient, on-demand network access to a shared pool of configurable computing resources (e.g., networks, servers, storage, applications, and services) that can be rapidly provisioned and released with minimal management effort or service provider interaction. This cloud model is composed of five essential characteristics, three service models, and four deployment models.*

## Essential Characteristics of Cloud Computing

### On Demand Self Service

It lets us get our servers and services deployed much more quick than we could with the traditional models. We are able to provision, monitor and manage computing resources as needed.

Lets think AWS and we want to use EC2 service and we enter some configurations values then when click to Create button, your application will be deployed quickly.

### Rappid Elasticty

You can spin up and make decommison your services quickly when it is required.

Lets give an example. We have an e-commerce application and we get higher seasonal demand on specific times. So we need to spin up at those times and while using cloud computing, we can automatically spin up servers as our demand eaisly and we can make decommison afterwards.

### Broad Network Access

The computing services are generally provided over standard networks and heterogeneous devices. Traditional way and cloud computer have same arhitect wtih that.

### Resource Pooling

- The cloud provider will make ensure we don't put too many VMs on any single servers.
- Storage are given customers exactly how much they are require.
- All tenants are going to have firewalls rules for controlling traffic. A pyhsical firewall is not given for every customer. Customer can share the same firewall. 

### Measured Service

The cloud provider needs to be able to measure how much of the service each customer is using. 

## Cloud Service Models

The NIST defines three Service Models as below;
- Iaas - Infrastructure as a Service
- Paas - Platform as a Service
- Saas - Software as a Service

These three models define  customer and provider's area of reponsibilities and customer's level of access.

Data Center Stack

```
-------------
Data
-------------
Applications
-------------
OS
-------------
Hypervisor
-------------
Compute
-------------
Storage
-------------
Network
-------------
Facility
-------------
```

At on premise all these thing are managed by customer.
At Colo facilities, customers can access Network level. 

#### 🚀 Hypervisor

Virtual machine is installed on it and there is OS and applications in it. When I installed the second VM, it has an OS and app too. But the OS in the second VM is the difference instance. These two VMs dont know each other so you can imagine that they are different server.

There two type of Hypervisor.

- Type 1 Hypervisor 

Type 1 Hypervisors run on the system hardware direcly and acts as OS. This is used in a data center.

- Type 2 Hypervisor 

Type 2 Hypervisors run on top of a host operating system.This is used in your laptop.


### Iaas - Infrastructure as a Service

The customer does not manage or control the underlying cloud infrastructure, but has control over OS. The service model gives customer the most control.

- Customers can install whichever applications they want to use on a VM.
- Customers can be offered to use shared or dedicated firewall and load balancer and they can connect into cloud provider over the internet or via direct network.
- Customers have internal or external storages options.
- Customers can manage their servers.
- Customers have application options. They can either install and look after or cloud provider can do it.

⚡️ There are some options as below.

- Different customer can have their virtual machines on the same shared underlying physical servers. It is the least expensive option and it needs less options in terms of how many RAM, CPU and storage)
- A customer is guaranteed that the underlying physical server is dedicated to them. This is more expensive optiona and it needs more options in term of RAM, CPU and storage.
- A customer is given access to their own physical servers. A hypervisor is not installed and managed by cloud provider. This option is the most expensive one and it needs the most options in term of RAM, CPU and storage (AWS does not offer this option).


⚡️ Billing 
- CPU and RAM will be billed when VM is power on.
- Network bandwidth will be billed when it is used.
- Data storage will be billed whetever the data is taking a pysical storage space.

⚡️ Examples; AWS EC2

### Paas - Platform as a Service

The provider will provide custom environment which is used for building application. The goal of Paas is to make it quicker for customers to able to get their applicartions into deployment. 

⚡️ Examples; AWS Elastic Beanstalk

### Saas - Software as a Service

Customesr will get in the application level so you will be able to work with the application but provider manages everthing.

⚡️ Examples; Microsoft Office 365, Gmail

 Desktop as a Service is Cloud based Virtual Desktop Infrastructure


#### 🚀 Data Protection
You need to provision Data Protection as part of your design, it is not done for you by default.

## Cloud Deployment Models

### Public
 Cloud providers sell their services to the general population.

 Example
 AWS, Microsoft Azure

 ### Private 
 Cloud providers sell their services to the organization's own internal business. I works same way with the Public but the differences is Private models fulfils the `Essential Characteristics of Cloud Computing`.
 This model is expensive due to a data center would be dedicated to just one customer. 

### Community
It allows systems and services to be accessible by a group of organizations.

### Hybrid Cloud

A company have private cloud but also use public cloud for their disaster recovery solutions.













