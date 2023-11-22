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

## Describe the consumption-based model
