
Azure Logging & Log Analytics Resources
====

### Microsoft Azure References
* [Get started with Log Analytics in the Azure portal](https://docs.microsoft.com/en-us/azure/azure-monitor/log-query/get-started-portal)
* [Get started with queries in Log Analytics](https://docs.microsoft.com/en-us/azure/azure-monitor/log-query/get-started-queries)
* [Search queries in Log Analytics](https://docs.microsoft.com/en-us/azure/azure-monitor/log-query/search-queries)


### Azure Firewall
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
      


### Azure Monitoring
* https://azure.microsoft.com/en-us/solutions/monitoring/


### Azure Monitor
* https://azure.microsoft.com/en-us/services/monitor/
* https://docs.microsoft.com/en-us/azure/azure-monitor/
  * https://docs.microsoft.com/en-us/azure/azure-monitor/azure-monitor-rebrand
    * "```Log Analytics and Application Insights have been consolidated into Azure Monitor``` to provide a single integrated experience for monitoring Azure resources and hybrid environments"
	* "None of the services that were part of OMS have changed, except for the consolidation into Azure Monitor"
	* ```Retirement of Operations Management Suite brand```
	  * "Operations Management Suite (OMS) was a bundling of the following Azure management services for licensing purposes:
	    * Application Insights
		* Azure Automation
		* Azure Backup
		* Log Analytics
		* Site Recovery
* https://docs.microsoft.com/en-us/azure/azure-monitor/overview
* https://docs.microsoft.com/en-us/azure/azure-monitor/app/distributed-tracing
* https://docs.microsoft.com/en-us/azure/azure-monitor/app/api-custom-events-metrics


### Application Insights
* [Analytics in Application Insights](https://docs.microsoft.com/en-us/azure/azure-monitor/app/analytics)
* [Azure Monitor Application Insights Documentation](https://docs.microsoft.com/en-us/azure/azure-monitor/azure-monitor-app-hub) - VERY USEFUL LINK
* https://docs.microsoft.com/en-us/azure/azure-monitor/app/app-insights-overview
  * "Application Insights is an extensible Application Performance Management (APM) service for web developers on multiple platforms. Use it to monitor your live web application. It will automatically detect performance anomalies. It includes powerful analytics tools to help you diagnose issues and to understand what users actually do with your app. It's designed to help you continuously improve performance and usability. It works for apps on a wide variety of platforms including .NET, Node.js and J2EE, hosted on-premises, hybrid, or any public cloud. It integrates with your DevOps process, and has connection points to a variety of development tools. It can monitor and analyze telemetry from mobile apps by integrating with Visual Studio App Center."
  * [Video: Application Insights Animated Introduction](https://www.youtube.com/watch?v=fX2NtGrh-Y0)
  * It montirs:
    * Request rates, response times, and failure rates - Find out which pages are most popular, at what times of day, and where your users are. See which pages perform best. If your response times and failure rates go high when there are more requests, then perhaps you have a resourcing problem.
    * Dependency rates, response times, and failure rates - Find out whether external services are slowing you down.
    * Exceptions - Analyse the aggregated statistics, or pick specific instances and drill into the stack trace and related requests. Both server and browser exceptions are reported.
    * Page views and load performance - reported by your users' browsers.
    * AJAX calls from web pages - rates, response times, and failure rates.
    * User and session counts.
    * Performance counters from your Windows or Linux server machines, such as CPU, memory, and network usage.
    * Host diagnostics from Docker or Azure.
    * Diagnostic trace logs from your app - so that you can correlate trace events with requests.
    * Custom events and metrics that you write yourself in the client or server code, to track business events such as items sold or games won.
  * https://docs.microsoft.com/en-us/azure/azure-monitor/app/proactive-diagnostics
  * https://docs.microsoft.com/en-us/azure/azure-monitor/app/app-map
  * https://docs.microsoft.com/en-us/azure/azure-monitor/app/profiler
  * https://docs.microsoft.com/en-us/azure/azure-monitor/app/usage-overview
  * https://docs.microsoft.com/en-us/azure/azure-monitor/app/diagnostic-search
  * https://docs.microsoft.com/en-us/azure/azure-monitor/app/metrics-explorer
  * https://docs.microsoft.com/en-us/azure/azure-monitor/app/app-insights-dashboards#dashboards
  * https://docs.microsoft.com/en-us/azure/azure-monitor/app/live-stream
  * https://docs.microsoft.com/en-us/azure/azure-monitor/app/analytics
  * https://docs.microsoft.com/en-us/azure/azure-monitor/app/visual-studio
  * https://docs.microsoft.com/en-us/azure/azure-monitor/app/snapshot-debugger
  * https://docs.microsoft.com/en-us/azure/azure-monitor/app/export-power-bi
* [Overview of Application Insights for DevOps](https://docs.microsoft.com/en-us/azure/azure-monitor/app/detect-triage-diagnose)
* [Diagnose exceptions in your web apps with Application Insights](https://docs.microsoft.com/en-us/azure/azure-monitor/app/asp-net-exceptions)
* [Video: Application Performance Management with Azure Application Insights](https://channel9.msdn.com/events/Connect/2016/112?ocid=player)


### Log Analytics
* [Channel 9 Video: Azure Log Analytics](https://channel9.msdn.com/Shows/Azure-Friday/Azure-Log-Analytics)
* [Custom logs in Log Analytics](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-sources-custom-logs)
* NOTE: ```Log Analytics is now a part of Operations Management Suite.```
  * https://azure.microsoft.com/en-us/services/virtual-machines/secure-well-managed-iaas/
* [Azure Log Analytics Feedback page](https://feedback.azure.com/forums/267889-log-analytics)
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


  
### Serilog
* https://serilog.net/
* https://github.com/serilog/serilog
  * Simple .NET logging with fully-structured events
  * "Serilog is a diagnostic logging library for .NET applications. It is easy to set up, has a clean API, and runs on all recent .NET platforms. While it's useful even in the simplest applications, Serilog's support for structured logging shines when instrumenting complex, distributed, and asynchronous applications and systems."
  * https://github.com/serilog/serilog/wiki/Getting-Started
  * https://github.com/serilog/serilog/wiki
* https://github.com/serilog/serilog-extensions-logging
  * A Serilog provider for Microsoft.Extensions.Logging, the logging subsystem used by ASP.NET Core.
* https://stackoverflow.com/questions/tagged/serilog
* nuget.org
  * [Serilog event sink that writes to Azure Analytics](https://www.nuget.org/packages/Serilog.Sinks.AzureAnalytics/)
	* https://github.com/saleem-mirza/serilog-sinks-azure-analytics
* Articles
  * 2017
    * [2017-04-26 ASP.NET Core Logging with Azure App Service and Serilog](https://blogs.msdn.microsoft.com/webdev/2017/04/26/asp-net-core-logging/)
  * 2016
    * [2016-07-01 Application logging to Azure using SeriLog](https://cmatskas.com/application-logging-to-azure-using-serilog/)
* stackoverflow.com
  * https://docs.microsoft.com/en-us/azure/azure-monitor/app/export-power-bi
* Pluralsight.com 
  * https://www.pluralsight.com/courses/modern-structured-logging-serilog-seq



### NLog
* https://nlog-project.org/
  * https://nlog-project.org/archives/
* https://twitter.com/NLogOfficial
* https://github.com/NLog/NLog/wiki
* https://github.com/NLog/NLog/wiki/Tutorial
* nuget.org	
  * https://www.nuget.org/packages/NLog.config
* https://github.com/NLog/NLog
  * Log - Advanced and Structured Logging for Various .NET Platforms
  * https://github.com/NLog/NLog/blob/master/CHANGELOG.md



### SlideShare presentations
* [What is going on? Application Diagnostics on Azure - Copenhagen .NET User Group](https://www.slideshare.net/maartenba/what-is-going-on-application-diagnostics-on-azure-copenhagen-net-user-group)
* 2018
  * [Azure Monitoring Overview](https://www.slideshare.net/gjuljo/azure-monitoring-overview?qid=86ecee85-46a5-4c4c-bc67-30faaecabb81&v=&b=&from_search=6)

