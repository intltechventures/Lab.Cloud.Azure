
Azure Logging & Log Analytics Resources
====

### Microsoft Azure References
* [Tutorial: Monitor Azure Firewall logs and metrics](https://docs.microsoft.com/en-us/azure/firewall/tutorial-diagnostics)
  * Activity logging is automatically enabled for every Resource Manager resource. Diagnostic logging must be enabled to start collecting the data available through those logs.
  * Diagnostic logs do not require a separate storage account. The use of storage for access and performance logging incurs service charges.
  * Important: Diagnostics must be turned on:
    * ```AzureFirewallApplicationRule```
    * ```AzureFirewallNetworkRule```
	
* [Azure Firewall Log Analytics samples](https://docs.microsoft.com/en-us/azure/firewall/log-analytics-samples)

* [Azure Firewall logs](https://docs.microsoft.com/en-us/azure/firewall/logs-and-metrics)
  * "The Application rule log is saved to a storage account, streamed to Event hubs and/or sent to Log Analytics only if you have enabled it for each Azure Firewall."
  * "The Network rule log is saved to a storage account, streamed to Event hubs and/or sent Log Analytics only if you have enabled it for each Azure Firewall."
  * You have three options for storing your logs:
    * "Storage account: Storage accounts are best used for logs when logs are stored for a longer duration and reviewed when needed."
    * "Event hubs: Event hubs are a great option for integrating with other security information and event management (SEIM) tools to get alerts on your resources."
    * "Log Analytics: Log Analytics is best used for general real-time monitoring of your application or looking at trends."

	
### Application Gatgeway
* Application Gateway 
  * [Back-end health, diagnostic logs, and metrics for Application Gateway](https://docs.microsoft.com/en-us/azure/application-gateway/application-gateway-diagnostics)
    * "In the portal, back-end health is provided automatically. In an existing application gateway, select ```Monitoring > Backend health```"

	
### Web Application Firewall (WAF)
* [Web application firewall (WAF)](https://docs.microsoft.com/en-us/azure/application-gateway/waf-overview)
  * "Monitor your web application against attacks using a real-time WAF log. This log is integrated with Azure Monitor to track WAF alerts and logs and easily monitor trends."
  * "WAF is integrated with Azure Security Center. Azure Security Center allows for a central view of the security state of all your Azure resources."
  * Diagnostic Logs
    * "You can use different types of logs in Azure to manage and troubleshoot application gateways. You can access some of these logs through the portal. All logs can be extracted from Azure Blob storage and viewed in different tools, such as Log Analytics, Excel, and Power BI. "
	  * "Activity log: You can use Azure activity logs (formerly known as operational logs and audit logs) to view all operations that are submitted to your Azure subscription, and their status. Activity log entries are collected by default, and you can view them in the Azure portal."
      * "Access log: You can use this log to view Application Gateway access patterns and analyze important information. This includes the caller's IP, requested URL, response latency, return code, and bytes in and out. An access log is collected every 300 seconds. This log contains one record per instance of Application Gateway. The Application Gateway instance is identified by the instanceId property."
      * "Performance log: You can use this log to view how Application Gateway instances are performing. This log captures performance information for each instance, including total requests served, throughput in bytes, total requests served, failed request count, and healthy and unhealthy back-end instance count. A performance log is collected every 60 seconds."
      * "Firewall log: You can use this log to view the requests that are logged through either detection or prevention mode of an application gateway that is configured with the web application firewall."
  * "Logs are available only for resources deployed in the Azure Resource Manager deployment model. You cannot use logs for resources in the classic deployment model."
    * [Azure Resource Manager vs. classic deployment: Understand deployment models and the state of your resources](https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-deployment-model)
  * "You have three options for storing your logs:"
    * "```Storage account```: Storage accounts are best used for logs when logs are stored for a longer duration and reviewed when needed."
    * "```Event hubs```: Event hubs are a great option for integrating with other security information and event management (SEIM) tools to get alerts on your resources."
    * "```Log Analytics```: Log Analytics is best used for general real-time monitoring of your application or looking at trends."
  * Enable logging through the Azure portal
    * In the Azure portal, find your resource and click Diagnostic logs.
      * For Application Gateway, three logs are available:
        * Access log
        * Performance log
        * Firewall log
      * To start collecting data, click Turn on diagnostics.
  * "Azure generates the activity log by default. The logs are preserved for 90 days in the Azure event logs store"
    * [View activity logs to audit actions on resources](https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-group-audit)
      * "The access log is generated only if you've enabled it on each Application Gateway instance"
      * "The activity log contains all write operations (PUT, POST, DELETE) performed on your resources. It doesn't include read operations (GET)."
        * what operations were taken on the resources in your subscription
        * who started the operation
        * when the operation occurred
        * the status of the operation
        * the values of other properties that might help you research the operation
      * "The performance log is generated only if you have enabled it on each Application Gateway instance"
        * "he data is stored in the storage account that you specified when you enabled the logging."
        * "The performance log data is generated in ```1-minute intervals```."
      * "The firewall log is generated only if you have enabled it for each application gateway"
      

### Log Analytics
* [Azure networking monitoring solutions in Log Analytics](https://docs.microsoft.com/en-us/azure/azure-monitor/insights/azure-networking-analytics)
  * "Log Analytics offers the following solutions for monitoring your networks:"
    * "Network Performance Monitor (NPM) to"
	  * "Monitor the health of your network"
	* "Azure Application Gateway analytics to review"
	  * "Azure Application Gateway logs"
	  * "Azure Application Gateway metrics"
	* "Solutions to monitor and audit network activity on your cloud network"
	  * "Traffic Analytics"
	  * "Azure Network Security Group Analytics"

* [Network monitoring solutions](https://docs.microsoft.com/en-us/azure/azure-monitor/insights/azure-networking-analytics)



### GoAccess log analyzer (for Application Gateway Access Logs)
* https://goaccess.io/
    * "GoAccess is an open source real-time web log analyzer and interactive viewer that runs in a terminal in *nix systems or through your browser. "
    * "It provides fast and valuable HTTP statistics for system administrators that require a visual server report on the fly. "
    * "We have published a Resource Manager template that installs and runs the popular GoAccess log analyzer for Application Gateway Access Logs. GoAccess provides valuable HTTP traffic statistics such as Unique Visitors, Requested Files, Hosts, Operating Systems, Browsers, HTTP Status codes and more."
  * https://goaccess.io/get-started
  * https://goaccess.io/features
  * https://goaccess.io/man
  * https://goaccess.io/faq
  * https://goaccess.io/release-notes
  * https://github.com/Azure/azure-quickstart-templates/tree/master/application-gateway-logviewer-goaccess
    * "This template configures the GoAccess log analyzer for Azure Application Gateway access logs. Using GoAccess, users can quickly analyze and view their Application Gateway statistics in real time using their browser through generated HTML reports."
    * "The template creates an Ubuntu VM under your (customer) subscription, installs Apache HTTP web server as well as the GoAccess log analyzer, and then connects the VM with the customer’s Blob container to periodically fetch incremental access logs of Application Gateway. GoAccess will parse the access logs and display rich statistics on traffic."




### Power BI
* https://powerbi.microsoft.com/en-us/
  * https://powerbi.microsoft.com/en-us/pricing/
  * https://docs.microsoft.com/en-us/power-bi/
  * https://powerbi.microsoft.com/en-us/blog/
  * https://community.powerbi.com/
* https://www.youtube.com/user/mspowerbi
* [View and analyze Azure Audit Logs in Power BI and more](https://azure.microsoft.com/en-us/blog/analyze-azure-audit-logs-in-powerbi-more/)




### Azure Insights SDK & Code Samples
* [Analyze Azure Audit Logs using Azure Insights SDK[(https://code.msdn.microsoft.com/Analyze-Azure-Audit-Logs-0977ada4)
  * "n this sample you can make use of the Azure Insights & Azure Resource Manager SDKs to dive deeper into Azure Audit Logs."
  * "The sample allows you to dump the audit logs for a given subscription and a number of days as a CSV file."

  * [Azure Networking Log Converter](https://github.com/Azure-Samples/networking-dotnet-log-converter) (2016)
  * The solution contains 5 executable console app projects:
    * CountersLogConverter
    * EventsLogConverter
    * OperationsLogConverter
    * LoadBalancerAlertLogConverter
    * LoadBalancerHealthProbeLogConverter.


  






