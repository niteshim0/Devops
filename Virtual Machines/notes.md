# Real World Analogy of Virtual Machine
We will understand it through an analogy from real world scenario:-
Suppose there is 1 acre of plain land and you have built a lavish house on that and you alongwith your family of say(4 members) move in that house and  leading your life happily and lavishly.

But over the time you come to realise that you don't utilize your whole land fully.
let's say 1/4 acre of land remains unutilized.So you decided to build a property on top of that and rent it now you have access to the rent as well.

So in this case your thinking is exact like devops in which you take something unefficient an make it efficient.

In the realm of computing, the concept of a virtual machine mirrors the optimization of available resources, much akin to the scenario of a lavish house on a vast expanse of land. Imagine possessing a powerful computer system, analogous to the grandeur of your house, where you and your family comfortably reside, leading a life of opulence.

However, as time unfolds, a realization dawns upon you – a substantial portion of the land remains underutilized, similar to the untapped potential in computing resources. In the world of DevOps, this inefficiency is not just acknowledged but strategically addressed. It parallels your decision to build additional property on the unused land, now generating additional income through rent.

In the digital landscape, a virtual machine serves as the solution, acting as a software-based emulation of a physical computer. This enables the efficient use of computing resources by running multiple virtual instances on a single physical server. Much like your initiative to make optimal use of the unutilized land, DevOps professionals leverage virtualization to transform initially underutilized computing infrastructure into a more efficient and versatile environment.

Through this approach, every facet of the "land" – the computing resources – is utilized to its full potential, not only optimizing resource utilization but also enhancing flexibility and scalability. The analogy encapsulates the essence of DevOps thinking, where the objective is to transform inefficiencies into efficiency, ensuring that every component contributes meaningfully to the overall productivity and performance.

# Virtual Machine and Virtualization

A Virtual Machine (VM) is a software-based emulation of a physical computer. It allows you to run an operating system (OS) and associated applications on a virtualized environment, isolated from the underlying hardware. This virtualization process enables multiple virtual machines to coexist on a single physical machine, each operating independently as if it were a standalone computer.

## Key Components of Virtual Machine :

### Hypervisor/ Virtual Machine Monitor (VMM):

This is the software or firmware responsible for creating and managing virtual machines. It sits between the hardware and the operating systems running on the virtual machines.

### Guest Operating System:

Each virtual machine runs its own operating system, known as the guest OS. This can be the same or different from the host operating system (the OS on the physical machine).

### Virtual Hardware:

The virtual machine has its own set of virtualized hardware resources, including virtual CPU, memory, storage, and network interfaces. These resources are managed by the hypervisor.

## Benefits of Virtual Machines:

### Resource Efficiency:
Multiple virtual machines can run on a single physical server, maximizing the use of resources and reducing hardware costs.

### Isolation:
Each virtual machine is isolated from others, providing a secure environment. Any issues or changes in one VM do not affect others.

### Flexibility and Scalability:
Virtual machines can be easily created, modified, and scaled up or down based on demand. This flexibility is valuable for dynamic and evolving computing needs.

### Testing and Development:
Virtualization allows developers and testers to create and run multiple environments on a single physical machine, making it easier to test software and applications in different scenarios.

### Legacy Application Support:
Virtual machines enable running older or legacy applications on modern hardware, helping in the transition to new infrastructure without sacrificing compatibility.

## Use Case of Virtual Machines:
Popular hypervisors include VMware, Microsoft Hyper-V, and open-source solutions like KVM (Kernel-based Virtual Machine) and VirtualBox. Virtualization is a fundamental technology in cloud computing, data centers, and modern IT infrastructure.


# Virtualization and Efficient Resource Utilization in Cloud Computing

Consider a scenario where AWS Services have established a data center in Mumbai, comprising 100 physical servers, each with a capacity of 100GB. In a non-virtualized environment, if someone requests a server with a size of 10GB, the entire physical server would need to be dedicated to fulfill that request.

## Without Virtualization:

- **Limited Resource Allocation:** Each physical server has a fixed capacity of 100GB, leading to underutilization when users request servers of varying sizes.

- **Resource Fragmentation:** Allocation becomes challenging, and the available capacity is not efficiently used, resulting in wasted resources.

- **Scalability Challenges:** Scaling based on demand is cumbersome without the ability to divide physical resources into smaller, more flexible units.

## With Virtualization:

Virtualization introduces the concept of Virtual Machines (VMs), where each physical server can be divided into multiple virtual machines, each with its own allocated resources.

- **Dynamic Resource Allocation:** When someone requests a server of 10GB, a virtual machine with the requested capacity can be provisioned on a physical server.

- **Optimized Utilization:** Multiple virtual machines of varying sizes coexist on a single physical server, maximizing resource utilization.

- **Scalability and Flexibility:** Virtualization enables easy scaling of resources based on demand, allowing for a more dynamic and responsive infrastructure.

### Example - Mumbai Data Center:

In the case of the AWS data center in Mumbai, virtualization allows for efficient allocation of resources. If 100 physical servers are available, virtualization enables the simultaneous provisioning of servers for numerous users with varying resource requirements. This flexibility optimizes the use of the data center's capacity, ensuring that it serves the needs of many users concurrently.

# Creating Virtual Machines on Cloud Providers

Virtual machines can be deployed in cloud environments, such as Amazon AWS, Microsoft Azure, or Google Cloud.

## AWS

To create a virtual machine on AWS, follow these steps:

1. Access the AWS Console in your browser.
2. Navigate to the EC2 service.
3. Create a virtual machine, which will return an EC2 instance.

## Azure

For Azure, the process is as follows:

1. Go to the Microsoft Azure portal in your browser.
2. Create a virtual machine, and it will return an instance (commonly known as a VM in Azure).

## Automation in DevOps

In scenarios where there are numerous requests for creating virtual machines within an organization, manual creation is not practical. DevOps aims to reduce manual labor and increase automation for improved efficiency.

### How to Automate the Process?

1. **AWS CLI:**
   - Use the AWS Command Line Interface to automate AWS tasks.

2. **AWS API (Boto3 in Python):**
   - Write scripts using the AWS SDK for Python (Boto3) to interact with AWS services programmatically.

3. **AWS CDK:**
   - Use the AWS Cloud Development Kit (CDK) to define cloud infrastructure using familiar programming languages.

4. **AWS CloudFormation (CFT):**
   - Write CloudFormation templates to define and provision AWS infrastructure.

5. **Terraform:**
   - Employ Terraform, a widely-used IaC tool, especially preferred in hybrid cloud environments.

### Automation Workflow:

1. User initiates the request to create an EC2 instance.
2. Verify user authentication and authorization.
3. Once verified, the service provider executes an automation script.
4. The script interacts with the chosen automation tool (CLI, API, CDK, CloudFormation, or Terraform).
5. The cloud provider returns the provisioned EC2 instance.

Automation improves repeatability, consistency, and scalability in managing virtual machines on cloud platforms.

# Scripts in Terms of Virtual Machines

In the context of virtual machines, a "script" typically refers to a set of instructions written in a scripting or programming language to automate various aspects of virtual machine deployment and management.

## Common Scenarios for Using Scripts:

### 1. Virtual Machine Provisioning:
Scripts can automate the creation of virtual machines on cloud platforms or virtualization environments. For example, deploying and configuring Amazon EC2 instances or Microsoft Azure VMs.

### 2. Configuration Management:
Scripts are used to automate the configuration of virtual machines, including tasks such as installing software, applying settings, and ensuring specific requirements are met.

### 3. Scaling and Orchestration:
Scripts or automation tools are employed to orchestrate the deployment and management of multiple virtual machines, facilitating dynamic resource scaling.

### 4. Infrastructure as Code (IaC):
Scripts are integral to Infrastructure as Code (IaC) practices, where languages like Terraform, AWS CloudFormation, or Azure Resource Manager templates define and manage the desired state of infrastructure, including virtual machines.

### 5. Lifecycle Management:
Scripts can automate tasks such as starting, stopping, or terminating virtual machines based on specific conditions or schedules.

### 6. Customization and Optimization:
Scripts allow users to customize virtual machine configurations based on specific requirements or optimize resource usage.

## Examples of Scripting Languages:

- **Bash/Shell Scripting:** Used for automating tasks on Linux-based virtual machines.
- **Python:** A versatile language used with SDKs like Boto3 for AWS automation or the Azure SDK for Python.
- **PowerShell:** Commonly used for scripting and automation on Windows-based virtual machines.
- **Terraform:** A declarative language for defining and provisioning infrastructure as code.

In summary, in the context of virtual machines, a script is a code artifact that automates tasks related to the creation, configuration, and management of virtualized infrastructure.
