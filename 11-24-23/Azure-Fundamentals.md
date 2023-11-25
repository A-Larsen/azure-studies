# Clean up
When you're working in your own subscription, it's a good idea at the end of a
project to identify whether you still need the resources you created. Resources
that you leave running can cost you money. you can delete resourcces
individually or delte the resource group to delete the entire set of resources.

# Check your Knowledge
1. Q: How many resource groups can a resource be in at the same time?

1. A: one

2. Q: What happens to the resources within a resource group when an action or
   setting at the resources group level is applied?

2. A: The setting is applied to current and future resources.

3. Q: What Azure feature replicates resources across regions that are at least
   300 miles away from each other

3. A: Region pairs

# Describe Azure virtual machines

- VMs -> **Iaas** in form of virtualized server

you can even create or use an already created image to rapidly provision VMs.
You can create and provision a VM in minutes when you select a preconfigured VM
image. An image is a template used to create a VM and may already include an OS
and other software, like development tools or web hosting environments.

# Scale VMs in Azure
You can run signle VMs for testing, development, or minor tasks. Or you can
group VMs together to provide high availability, scalability, and redundancy.
Azure can also manage the grouping of VMs for you with features such as scale
sets and availability sets.

# Virtual machine scale sets
Scale sets help you manage multiple a large number of VMs. the number of VM
instances can automatically increase or decrease in response to demand, or you
can set it to scale based on a defined schedule.

- automatically deploy a load balancer

# Virtual machine availability sets

* **Update domain**: the update domain groups VMs that can be rebooted at the
  same time. An update group going through the update process is given a
  30-minute time to recover before maintenance on the next update domain starts.

* **Fault domain**: The fault domain groups your VMs by common power resource
  and network switch. By default, an avaqilability set will split your VMs
  across up to three fault domains.

- no additional cost for configuring an availability set. You only pay for the
  VM instance you create

# Example of when to use Vms

* During testing and development

* When running applications

* When extending your datacenter to the cloud. Some application can be ran in
  the cloud

* During distaster recovery. save money with Iaas-based approach to distaster
  recovery. If a primary datacenter fails, you can create VMs running on Azure
  to run your critical applications when needed.

# Move to the cloud with VMs
- **lift and shift**: moving from a physical server to the cloud.

You can create an image of the physical server and host it within a VM with
little or no changes. responsible for installed OS and software.

# VM Resources
When you provision a VM, you'll also have the chance to pick the resources that
are associated with that VM, including:

- **Size**: (purpose, number of processor cores, and amount of RAM)
- **Stroge disks**: (hard disk drives, solid state drives, etc)
- **Networking** (virtual network, public IP address, and port configuration)

# Exercise - Create an Azure virtual machine

## Create a Linux virtual machine and install Nginx

```sh
az vm create \
  --resource-group learn-e9c1003f-3b05-46d6-b4b6-e3db182d3743 \
  --name my-vm \
  --public-ip-sku Standard \
  --image Ubuntu2204 \
  --admin-username azureuser \
  --generate-ssh-keys
```

```sh
az vm extension set --resource-group learn-e9c1003f-3b05-46d6-b4b6-e3db182d3743 --vm-name my-vm --name customScript --publisher Microsoft.Azure.Extensions --version 2.1 --settings '{"fileUris":["https://raw.githubusercontent.com/MicrosoftDocs/mslearn-welcome-to-azure/master/configure-nginx.sh"]}' --protected-settings '{"commandToExecute": "./configure-nginx.sh"}'
```
summary of the above script:

*  Runs `apt-get update`to download the latest package information from the
   internet. This step help ensure that the next command can locate the latest
   version of the Nginx package.

* Installs Nginx

* Sets the homepage, _/var/www/html/index.html_, to print a welcome message that
  includes you VM's host name.

# Describe the Azure Virtual desktop
- Another type of virtual machine

- **Azure Virtual Desktop**: a desktop and application virtualization service
  that runs on the cloud.l It enables you to use a cloud-hosted version fo
  Windows from any location. Azure Virtual Desktop works across devices and
  operating systems, and works with apps that you can use to access remote
  desktops or most modern browsers.

- solution for enabling central managment security of your users desktops

- less it managment overhead

- seperates your operating system, data, and apps from local hardare

- seprate compute enviornemt from user devices, so that the risk of confedential
  information being left on a personal device is greatly reduced.

- You can make sure that your personal machines run in close proximity to apps
  and services that connect to your datacenter or cloud.

- freedom to connect with any device over the internet

- For I.T you don't have to worry as much about the device that's connecting, as
  long as the network connection is secure.

- You can handle you're web access, Diagnostics, Gateway, Broker, Load balancing
  and more

- All your VMs in the windows virtual desktop service communicate of secure
  outbound connectiona and you benifit from unlimited capacity.

- Can choose any size VM in Azure

- Vary the density of users based on the workload.

- More choice how you destibute users accrosed those VMs.

- You're not limited to a windows server OS in cases where you want to assign
  more than one user per virtual machine. 

- With windows 10 enterprise multisession. you can gain efficiences by having
  mutliple users on a single VM. has supprot for modern apps like OneNote and
  Office 365.

- You can deploy a full desktop, remote apps, or both

- can scale up or scale down as needed, while paying only for what you use.

- Desktop Same as your local PC

- The only indication the app is virtual is throught the glif (might have
  spelled that wrong)

## Enchance Security
Azure Virtual Desktop provides centralized securtity managment fro users'
desktops with Microsoft Entra ID. you can enable multifactor authentication to
secure user sign-ins. You can also secure acccess to data by assigning granular
role-based controls (RBACs) to users.

user sessions are isolated in both signle and muti-session environments.

## Muti-session Windows 10 or Windows 11 deployment
Can use Windows 10 or Windows 11 Enterprise multi-session, the only Windows
client-based operating system that enables mutiple concurrent users on a single
VM.
Azure Virtual Desktop also provides a more consistent experience with braoder
application support compared to Windows Server-based operating systems.

# Describe Azure containers
- Allows mutiple instances of an application on a single host machine

- Not limited to a single operating system

## What are containers?
- can run multiple on a signle physical or virtual host.

- don't manage operating system

- appear to be an instance of an operating system that you can connect to and
  manage

- lightweight and designed to be created, scaled out, and stopped dynamically

- can quickly restart in emergency

- Docker is an example

## Compare virtual machines to containers

### Virtual Machines (VMs)

#### Pros
- provide an abstraction layer for CPU, memory, and storage. Can be changed,
  while allowing the enviornment to be flexable and secure.

- app runs either in isolation, or with other apps you've installed in VM.

- virtualize hardware

- can completly control the enviornment

#### Cons

- issolated from other applications

- can only run one operating system at a time

- some tasks are slow, (like starting up the VM)


### Containers
- Bundles a single app and its dependencies (refered to as containerizing the
  app), then deploys it as a unit to a container host. The container host
  provides a standardized runtime enviornment which abstacts away the operating
  system and infastructure requirements, allowing the containerizing application
  to run side by side with other containerized apps.

- Lighter weight as opposed to VMs

- virtualize the operating system

- more efficient than a full virutal machine

- **NOT** issolated from other applications

- Azure supports several container variation (Most popular is Docker)

- containerized apps are much smaller in size

- Development process is simplified, because your developemnt runtime
  enviornment can look exactly like the production enviornment.

- Can be orchestrated with container cluster orchestration

- You can easilty deploy and manage multiple containerized applications without
  worring about which server will host each container

- can **NOT** completly control the enviornment

## Azure Container Instances
- fastest and simplest way to run a container in Azure

- are Paas (Platform as a service)

## Azure Container Apps

- Similar to a container instance

- Paas offering

- Extra benifits such as the ability to incorporate load balancing and scaling

## Azure Kubernetes Service (AKS)
- A container orchestration service

An orchestration service manages the lifecycle of containers. When you're
deploying a fleet of containers, AKS can make fleet managment simpler and more
efficient.

## Use containers in your solutions
Containers are often used to create solutions by using a microservice
architecture. This solution is where you break solutions into smaller,
independent pieces. For example, you might split a website into a container
hosting your front end, another hosting our back end, and a third for storage.
this split allows you to seperate portions of your app into logical sections
that can be maintained, scaled, or updated independently.

## Describe Azure Functions
