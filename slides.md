---
marp: true
---

<!-- _class: invert -->

## Flatcar Container Linux

* A community Linux distribution designed for container workloads, with high
  security and low maintenance

* The introduction of container-based infrastructure was a paradigm shift. A
  Container-optimized Linux distribution is the best foundation for cloud native
  infrastructure.

---

## What is a Container Linux?

### Container

* A minimal OS image only includes the tools needed to run containers. No
  package manager, no configuration drift.

### Filesystem

* Delivering the OS on an immutable filesystem eliminates a whole category of
  security vulnerabilities.

### Update

* Automated atomic updates mean you get the latest security updates and open
  source technologies.

---

## Immutable Infrastructure

* Your immutable infrastructure deserves an immutable Linux OS. With Flatcar
  Container Linux, you manage your infrastructure, not your configuration.

---

## Designed to Scale

* Flatcar Container Linux includes tools to manage large-scale, global
  infrastructure. You can manage update polices, versions and group instances
  with ease.

---

## Reduced Complexity

* With containers, dependencies are packaged and delivered in container images.
  This makes package managers unnecessary and simplifies the OS.

---

## Secure by Design

* Flatcar Container Linux's built-in security features, minimal design and
  automated updates provide a strong foundation for your infrastructure's
  security strategy.

---

## Minimal Attack Surface

* Flatcar Container Linux includes only what is required to run containers. By
  minimizing the size and complexity of the OS, the attack surface is also
  reduced.

---

## Self-Driving Updates

* Flatcar Container Linux uses the same reliable update mechanism as Google’s
  ChromeOS to provide safe, secure and automated system updates.

---

## Managed Updates

* The Kinvolk Update Service allows for defining instance groups, assigning
  update channels and controlling the frequency, time of day and rate of
  updates.

---

## Kubernetes is Deployed On More Than 80% Flatcar Deployments

* Since Flatcar is designed for containers and Kubernetes is the most popular
  container orchestration system, 82% of Flatcar users reported that they ran
  Kubernetes in a recent Flatcar community survey.

---

## Kubeadm is the most popular Kubernetes deployment tool

* We asked those users were asked which Kubernetes distro or installation tool
  they were using. Even among a relatively small sample size, there was a wide
  variety of solutions in use, indicating that the Kubernetes landscape is still
  very heterogeneous. The most widely used tool, however, was kubeadm,
  reflecting that project’s position as the canonical upstream “best practice”
  installer.

---

## Three Quarters of Flatcar Users Deploy In Their Own Data Centers

* Users deploy Flatcar in a wide variety of environments: including all the
  major clouds, on-premises with vSphere, on-premises bare metal, and more.
  Looking at just cloud vs on-prem, we see that hybrid is the most popular
  option with users deploying some workloads on-prem and some in cloud.

---

## Most Flatcar Users Automate Updates

* Flatcar was designed to be an auto-updating operating system, inheriting the
  A/B partition and automatic update downloading mechanism from ChromeOS. More
  than 6 out of 10 users make use of this automatic update mechanism to ensure
  their systems stay always up to date. The remaining 37% reinstall nodes as
  required when new builds are available.

---

## Security and Manageability are Key Reasons for Deploying Flatcar

* Flatcar’s combination of automatic updates with an immutable base OS image are
  designed to make large distributed systems both more secure and easier to
  manage. This is reflected in the fact that 93% of users rated security and
  manageability as “somewhat” or “very” important factors in their decision to
  deploy Flatcar.

---

## Microsoft Acquired Kinvolk In April 2021

* **Kinvolk** has a rich, innovative history in open source cloud-native
  distributed computing, including Kubernetes, eBPF, community building, and
  container-optimized Linux, as well as critical early work with CoreOS (the
  company) on the rkt container runtime.

  * Kinvolk ultimately went on to create Flatcar Container Linux, a popular
    alternative to CoreOS Container Linux, as well as the Lokomotive and
    Inspektor Gadget projects.

* Microsoft plans to bring the expertise of the Kinvolk team to Azure, where
  they will be key contributors to the engineering development of Azure
  Kubernetes Service (AKS), Azure Arc, and future projects that will expand
  Azure’s hybrid container platform capabilities and increase Microsoft’s
  upstream open source contributions in the Kubernetes and container space.

---

## Transition To CGroupsV2

* Flatcar Container Linux v2969.0.0 was released to the Alpha channel on Aug 19,
  2021 and switched the default control groups hierarchy to CGroupsV2.

* Linux **namespaces** and control groups (or **cgroups**) are the core building
  blocks of containers on Linux. Cgroups restrict the resources (CPU, memory,
  I/O) that a process or container can consume, which is essential to securely
  hosting diverse workloads on the same system.

---

## Transition To CGroupsV2 (II)

* Cgroups were merged into the Linux kernel in 2008, long before projects such
  as Docker and Kubernetes were released. Shortcomings in the design of cgroups
  led to the release of CGroupsV2 (unified cgroup hierarchy) with Linux 4.5.

* The most significant difference between CGroupsV1 and CGroupsV2 is that,
  whereas in v1 control groups applied to each resource separately, in v2 there
  is a single (unified) hierarchy of control groups which apply across all
  resources.

---

<!-- _class: invert -->

## Demo Time

* In the following demo

  * we launch a flatcar instance with containerd,

  * login via ssh, and

  * look at */proc/version* and *cat /etc/os-release*,

  * look at the read-only status of /usr,

  * get a better understanding of boot partition A, and

  * list information on cgroupv2. 
