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
