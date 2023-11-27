# Microsoft Azure Funamentals

- [Ways to prepare](https://learn.microsoft.com/en-us/credentials/certifications/exams/az-900/#two-ways-to-prepare)

## Describe Cloud Concepts

- [Describe cloud concepts](https://learn.microsoft.com/en-us/training/paths/microsoft-azure-fundamentals-describe-cloud-concepts/)

- **Iaas**: Infastructure as a service
- **Saas**:  Sofware as a service
- **Paas**: Platform as a service

![Responsibility Model](https://learn.microsoft.com/en-us/training/wwl-azure/describe-cloud-compute/media/shared-responsibility-b3829bfe.svg)

The cloud provider is always responsible for:

- The pyhsical datacenter
- The physical network
- The physical hosts

## Define cloud models

Three cloud types: Private, public, and hybrid

### Private Cloud

- Used by a single entity 

> [!NOTE]
> My assumption is that they use the word "entity" because it might be controlled by
> other means than by human interaction. Maybe bots are used?

- Greater cost and fewer of the benefits of a public cloud deployment

- Greater control

- You decided where it is hosted

- No General public availablity

### Public cloud

- Third party

- Anyone that wants to puchase cloud services can access and use resources

- General public availablity

### Hybrid cloud

- Uses both public and private coulds in an inter-connected environment

- Allows a private cloud to surge for increased, temporary demand by deploying
  public could resources

- Can provide extra layer of security

- Chose what is in the public an private cloud

```table
| Public cloud     | Private cloud   | Hybrid cloud   |
|==================|=================|================|
| no captial       | organizations   | Provdes the    |
| expenditures     | have complete   | most           |
| to scale up      | control over    | flexability    |
|                  | resources and   |                |
|                  | security        |                |
|------------------|-----------------|----------------|
| Applications     | Data is not     | Organizations  |
| can be quickly   | collected with  | determine      |
| provisioned and  | other           | where          |
| deprovisioned    | organizations'  | to run their   |
|                  | data            | applications   |
|------------------|-----------------|----------------|
| Organizations    | hardware must   | Organizations  |
| pay only for     | be purchased    | control        |
| what they use    | for startup     | secutiry.      |
|                  | and maintenance | compliance, or |
|                  |                 | legal          |
|                  |                 | requirements   |
|------------------|-----------------|----------------|
| organizations    | Organizations   |                |
| dont's have      | are responsible |                |
| complete control | for hardware    |                |
| over resources   | maintenance and |                |
| and security     | updates         |                |
```

### Multi-cloud
You work with two (or more) public cloud providers and manage resources and
security in all of your environment

### Azure Arc
- Helps you manage you cloud environment
- could be a public, private, hybrid, or mutli-cloud environment

### Azure VMware Solutions
Lets yo run you VMware workloads in Azure with seamless integration and scalability

## Describe the high availability and scalability in the cloud

### High availability
You'll have to consider how long you wont your clouds uptime.

SLA's are service level agreements that are different dending on the percentage of up
time. You cannot have a 100% uptime. but you can have a 99.99 precent uptime.
each azure service has its own SLA.

- **99% downtime**: 1.68 hours per week
- **99.99% downtime**: 10 minutes per week

### Scalability
- ability to ajust cloud resources to meet a demand
- no overpaying for services
- only pay for what you use
- Vertical and horizontal scaling


### verical scaling
Abliity to cahnge if you need more or less computing resources (CPU, RAM, etc)

### Horizontal scaling
Ability to scale out and add additional virtual machines or containers, or scale
down in and have less.

## Descibe the benifits of reliability and predictability in the cloud

### Reliability
- **Reliability**: the ability of a system to revover from failures and continue
  to function

- cloud is decentralized. 

- allows recources to be deployed in regions around the world.

- In some cases, your cloud evnironment itself will automatically shift to a
  different region for you

### Predictability
- Performance or cost predictability

#### Performance

- **predictablity**: autoscaling, load balancing, and high availability

#### Cost

- focused on predicting the cost

- monitor resources for efficientcy

- apply data analytics to find patterns to help plan resource deployments, p

- predict future cost and adjust you resources as needed.

- can use tools like Total cost Ownership (TCO) or Pricing Calculator to get an
  estimate of protential cloud spending

## Describe the benifits of security and governance in the cloud

- Things like templates help ensure that all your deployed resources meet
  corporate standards and government regulatory requirements.

- Update all your deployed resources to new standards as standards change.

- Infrastructure as a service provides you with physical resources but lets you
  manage the operating systems and installed software, including patches and
  maintenance.

- Pratform as a service or software as a service patches and takes care of
  maintenance for you

- Well suited to handle things like distrobuted denial of service (DDos) attacks

## Describe the benefits of manageability in the cloud
Two types of manageability

### Managment of the cloud
In the cloud you can:

- Automatically scale resources deployment based on need.

- Deploy resources based on preconfigured template, removing the need for manual
  configuration

- Monitor the health of resources and automatically replace failing resources

- Receive automatic alerts based on configured metrics, so you're aware of
  performace in real time

### Managment in the cloud
You can manage these:

- Through the web portal

- using the command line interface

- Using APIs

- Using Powershell

## What is Microsoft Azure
- supportes Saas, Paas, Iaas

- serivices such as: virtual machines in cloud, website and database hosting, and
  advanced computing services such as ai, machine learning and iot

- You only pay for the computing time that you use

- Provides cloud based storage

- you can install a virtual machine from scratch, upload your own virtual
  harddrive, choose from templates they provides

- scalable hosting platform

- Azure functions allow you to create event driven serverless applications

- Azure container instances and Azure Kubernetes services allow you to deploy
  containerized allications with fully managed services

- offers fully managed relational and in-memory databases, spanning proprietory
  and open-source engines.

- microsofts cosmos DB provides support for several popular no SQL APIs.

- Has machine learning and artifician inteligence services

- Azures regional datacenters allow you to distribute your applications globaly.
  This helps improve application performance

- Azure portal allows you to create, configure and control all your resources
  from a single web based interface.

- Get security form the ground up, backend by a team of experts, an proactive
  compliance trusted by enterprises, governments, and startups.

## What can I do With Azuer?

- Provides more than 100 services

- Provides artificial intelligence (AI) and machine-learning (ML) services
  that can naturally communicate with your users through vision, hearing, and
  speech.

## Get started with Azure accounts

### Subscriptions
- learning modules create a termporary subscription
- Creating an Azure account will create a subscription for you. 
- you can create additional subscription if needed.
- you can create azure resources within each subscription

Many of the learn exercises use a technology called the sandbox, which creates a
termporary subscription that's added to your Azure account. This is no
additional cost

## Describe Azure physical infrastructure
The Core architectural components of Azure may be broken down into two main
groupings: the physical infrastructure, and the managment infrastructure

### Physical Infrastructure

- starts with the datacenters. 

- Datacenters aren't directly accessable

- Grouped into Azure Regions or Azure Availability zones that are designed to
  help you achieve resiliency for your business-critical workloads

### Regions
A **region** is a geographical area on the planet that contains at least one,
but potentially multiple datacenters that are nearby and networked together with
a low-latency network. Azure intelligetly assigns and controls the resources
within each region to ensure workloads are appropriately balanced.

When you deploy a resource in Azure, you'll often need to choose the region
where you want your resourc deployed.

### Availability Zones
**Availability zones** are physically separate datacenters within an Azure
region. Each Availability zone is made up of one or more datacenters equipped
with independent power, cooling, and networking. An availability zone is set up
to be an isolation boundry. If one zone goes down, the other continues working.
Availability zones are connected through high-speed, private fiber-optic
networks.

![Azure Region](https://learn.microsoft.com/en-us/training/modules/describe-core-architectural-components-of-azure/5-describe-azure-physical-infrastructure)

> [!IMPORTANT] 
> To ensure resiliency, a minimum of three separate availability zones are
> present in all availability zone-enabled regions. However, not all Azure
> Regions currently support availability zones.

## Use availability zones in your apps

- Create redundancy by using duplicate hardware environments. Azure can help
  maker you app highly available through availability zones.

- make high-availability by co-locating compute, storage, networking, and data
  resources within an availability zone and replicating in other availibity
  zones.

- could be a cost to duplicating your services and transfering between
  availability zones

- mission-critical applications

- primarly for: VMs, managed disks, load balancers, and SQL databases

- three categories

    * **Zonal services**: You pine the resource to a specific zone (for example,
      VMs, managed disks, IP addresses).

    * **Zone-Redundant services**: The platform replicates automatically
        across zones (for example, zone-redundant storage, SQL Database)

    * **Non-regional services**: Services are always available from Azure
      geographies and are resilient to zone-wide outages as wel as region-wide
      outages.

Even with the additional resiliency that availability zones provide, it's
possible that an event could be so large that it impacts multiple availability
zones in a single region. To provide even further resilience, Azure has Region
Pairs.

## Region pairs

- Most regions are paired within 300 miles

    * reduces likelihood of interruption that affect a region

## Additional advantages of region pairs

- If an extensive Azure outage occurs, one region out of every pair is
  prioritized to make sure at least one is restored as quickly as possible for
  applications hosted in that region pair.

- Planned Azure updates are rolled out to paired regions one region at a time to
  minimize downtime and risk of application outage

- Data continues to reside within the same geography as its pair (some
  exceptions)

## Sovereign Regions

- **Sovereign regions**: Instances of Azure that are isolated from the main
  instance of Azure.

- may ne3ed to use for compience or legal purposes.

## Describe Azure management infrastructure

- **managment infrastructure**: Azure resoureces, resource groups,
  subscriptions, and accounts.

- Understand this to help you plan your projects and products with Azure

## Azure resources and resource groups
