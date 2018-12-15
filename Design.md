
Azure Design Resources
====

### Microsoft Azure Docs
* [Azure Architecture](https://docs.microsoft.com/en-us/azure/index#pivot=architecture)
* [Azure Architecture Center](https://docs.microsoft.com/en-us/azure/architecture/)
  * [Ten design principles for Azure applications](https://docs.microsoft.com/en-us/azure/architecture/guide/design-principles/)
    * Design for self healing. In a distributed system, failures happen. Design your application to be self healing when failures occur.
    * Make all things redundant. Build redundancy into your application, to avoid having single points of failure.
    * Minimize coordination. Minimize coordination between application services to achieve scalability.
    * Design to scale out. Design your application so that it can scale horizontally, adding or removing new instances as demand requires.
    * Partition around limits. Use partitioning to work around database, network, and compute limits.
    * Design for operations. Design your application so that the operations team has the tools they need.
    * Use managed services. When possible, use platform as a service (PaaS) rather than infrastructure as a service (IaaS).
    * Use the best data store for the job. Pick the storage technology that is the best fit for your data and how it will be used.
    * Design for evolution. All successful applications change over time. An evolutionary design is key for continuous innovation.
    * Build for the needs of business. Every design decision must be justified by a business requirement.
  * [Design for self healing](https://docs.microsoft.com/en-us/azure/architecture/guide/design-principles/self-healing)
* [Azure Resiliency](https://azure.microsoft.com/en-us/features/resiliency/)
* [Autoscaling](https://docs.microsoft.com/en-us/azure/architecture/best-practices/auto-scaling)
* [Designing resilient applications for Azure](https://docs.microsoft.com/en-us/azure/architecture/resiliency/)
* [Availability checklist](https://docs.microsoft.com/en-us/azure/architecture/checklist/availability)
* [Scalability checklist](https://docs.microsoft.com/en-us/azure/architecture/checklist/scalability)
* [Microsoft Azure Storage Performance and Scalability Checklist](https://docs.microsoft.com/en-us/azure/storage/common/storage-performance-checklist)
* [Troubleshooting allocation failure when you deploy Cloud Services in Azure](https://docs.microsoft.com/en-us/azure/cloud-services/cloud-services-allocation-failures)
* [Managing Concurrency in Microsoft Azure Storage](https://docs.microsoft.com/en-us/azure/storage/common/storage-concurrency?toc=%2fazure%2fstorage%2fblobs%2ftoc.json)
* [Using the Retry pattern to make your cloud application more resilient](https://azure.microsoft.com/en-us/blog/using-the-retry-pattern-to-make-your-cloud-application-more-resilient/)



### Interesting Azure/Cloud Related Articles
* 2017
  * [Gray failure: the Achilles’ heel of cloud-scale systems](https://blog.acolyer.org/2017/06/15/gray-failure-the-achilles-heel-of-cloud-scale-systems/)
    * https://www.cs.jhu.edu/~huang/paper/grayfailure-hotos17.pdf
* 2016 
  * [The first time Microsoft engineers tried to use their own cloud, they failed](https://www.businessinsider.com/the-first-time-microsoft-engineers-tried-to-use-its-cloud-they-failed-2016-12)
  * [Why Microsoft Azure Stack is destined to fail](https://searchwindowsserver.techtarget.com/opinion/Why-Microsoft-Azure-Stack-is-destined-to-fail)
* 2014
  * [10 things I learned about rapidly scaling websites with Azure](https://www.troyhunt.com/10-things-i-learned-about-rapidly/)
  * [Video: Avoiding Cloud Fail: Learning from the Mistakes of Azure with Mark Russinovich](https://azure.microsoft.com/en-us/resources/videos/avoiding-cloud-fail-learning-from-the-mistakes-of-with-mark-russinovich/)
