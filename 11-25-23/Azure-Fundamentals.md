# Describe Azure functions

## Serverless computing in Azure
Serverless computing is a bit of a misleading name because their are servers
being used

- **serverless computing**: the responsability of managing servers is already
  handled for you

serverless computing is event driven. resources are only allocated from a direct
action. You are only charged for the time it takes to run your code. Instead of
paying for the resources if they're not being used.

## Benefits of Azure functions

- commonly used when you need to perform work in response to an event (often via
  a REST request), timer, or message form another Azure service.

- scale automatically based on demand

- Automatically deallocates resources when the function is finished

Functions can be either stateless or stateful. When they're stateless (the
default), they behave as if they're restarted every time they respond to an
event. When they're stateful (called Durable Functions), a context is passed
through the function to track prior activity.

- can still change to environment that isn't serverless.

# Describe the application hosting options

## Azure App Service

App service enables you to build and host wweb apps, background jobs, mobile
back-ends, and RESTful APIs int eh programming language of your choice without
managing infrastructure.

- offers automatic scaling ad high availability

- support windows ad linux.

- enables deployment from GitHub, Azure DevOps, or any Git repo to support
  continuous deployment model.

  Azure App Service is an HTTP-based service for hosting web applications, RECT
  APIs, and mobile back ends. It supports multiple languages, includign .NET,
  .NET core, Java, Ruby, Node.js, PHP, or Python, It also supports both Windows
  and Linux environements.

## Types of app Services

can host service styles like:

- Web apps
- API apps
- Webjobs
- Mobile apps

App Serice handles most of the infrastructure descisions you deal with in
hosting web-accessible apps:

- Deplayment and managment are integrated into the platform
- Endpoints can be secured
- Sites can be scaled quickly to handle high traffic loads
- The build-in load balancing and traffic manager provide high availability

## Web apps
App service includes full support for hosting web apps by using ASP.NET, ASP.NET
Core, Java, Ruby, Node.js, PHP, or Python, You can choose either Windows or
Linux as the host operating system.

## API apps
- can build REST-based web APIS using whatever

## WebJobs
You can use the webJobs feature to run a program (.exe, Java, Python, or
Node.js) or script (.cmd, .bat, Powershell, or bash) in the same context as a
web app, API app, or mobile app. They can be scheduled or run by a
trigger. Webjobs are often used to run background tasks as part of your
application logic.

## Mobile apps
Use the Mobile Apps feature of App Service to quickly build a back end for iOS
and Android apps. With just a few actions in the Azure portal, you can:

- Store mobile app data in a cloud-based SQL database

- Authenticate customers against common social providers, such as MSA, Google,
  Twitter, and Facebook

- Send push notifications

- Execute custom back-end logic in C# or Node.js

On the mobile app side, there's SDK support for native iOS and Android, Xamarin,
and React native apps

## Describe Azure Virtual networking
Azure virtual networks and virtual subnets enable Azure resources, such as VMs,
web apps, and databases, to communicate with each other, with users on the
internet, and with your on-premises client computers. You can think of an Azure
network as an extension of you on-premises network with resources that link
other Azure resources.

Azure virtual networks provide the following key networing capabilies:

- Isolation and segmentation

- Internet communications

- Communicate between Azure resources

- Communicate with on-premises resources

- Route network taffic

- Filter network traffic

- connect virtual networks

Azure virtual networking supports both public and private enpoints to enable
communication between external or internal resources with other internal
resources.

- Public endopints have a public IP address and can be accessed from anywhere in
  the world.

- Private endpoints exist within virtual network and have a private IP address
  from within the address space of that virtual network.

## Isolation and segmentation
Azure virtual network allows you to create multiple isolated virtual networks.
When you set up a virtual network, you define a private IP address space by
using either a public or private IP address ranges. The IP range only exists
within the virtual network and isn't internet routable. You can divide that IP
address space into subnets and allocate part of the defined address space to
each named subnet.

For name resolution, you can use the name resolution service that'sbuilt into
Azure. You also can configure the virtual network to use either an internal or
external DNS server.

## Internet communications
You can enable incoming connections form the internet by assigning a public IP
address to an Azure resource, or putting the resource behind a public load
balancer.

## Communicate between Azure resources
You'll want to enable Azure resources to communicate securely with each other.
You can do that in one of two ways:

- Virtual networks can connect not only VMs but other Azure resources, such as
  the App Service Environment for Power Apps, Azure Kubernetes Service, And
  Azure virtual machine scale sets

- Service endpoints can connect to other Azure resource types, such as Azure SQL
  databases and storage accounts. This approach enable you to link multiple
  Azure resources to virtual networks to improve security and provide optimal
  routing between resources

## Communicate with on-premises resources
Azure virtual networks enable you to link resources together in you on-premises
environment and within your Azure subscription. In effect, you can create a
network that spans both your local and cloud environments. These are three
mechanisms for you to achieve this connectivity:

- **Point-to-site** virtual private network connections are form a computer outside
  your organization back into your corporate network. In this case, the client
  computer initiates an encrypted VPN connection to connect to the Azure virtual
  network.

- **Site-to-site** virtual private networks link your on-premises VPN device or
  gateway to the Azure VPN gateway in a virtual network. In effect, the devices
  in Azure can appear as being on the local network. The connection is encrypted
  and works over the internet.

- **Azure ExpressRoute** provides a dedicated private connectivity to Azure that
  doesn't travel over the internet. ExpressRoute is useful for environments
  where you need greater bandwidth and even higher levels of security.

## Route network traffic
Azure virtual nnetworks enable you to filter traffic between subnets byusing the
following approaches:

- **network security groups** are Azure resources that can contain multiple inbound
  and outbound security rules. You can define these rules to allow or block
  traffic, based on factors such as source and destination IP address, port and
  protocol

  
- **Network virtual appliances** are specialized VMs that can be compared to a
  hardened network appliance. A network virtual appliance carries out a
  particular network function, such as running a firewall or performing wide
  area network (WAN) optimization.

## Connect virtual networks
You can link virtual networks together by using virtual nework peering. Peering
allows two virtual networks to connect directly to each other. Network traffic
between peered networks is private, and travels on the Microsoft backbone
network, never entering the public internet. Peering enables resources in each
virtual network to communicate with each other. These virtual networks can be in
seperate regions, which allows you to create a global interconnected network
through Azure.

User-defined routes (UDR) allow you to control the routing tables between
subnets within a virtual network or between virtual networks. This allows for
greater control over network traffic flow.

## Exercide - Configure network access
