
Azure Web Application Firewall (WAF) Resources
==== 

### Azure References
* https://docs.microsoft.com/en-us/azure/application-gateway/overview

* https://docs.microsoft.com/en-us/azure/application-gateway/waf-overview
  * "Web application firewall (WAF) is a feature of Application Gateway that provides centralized protection of your web applications from common exploits and vulnerabilities."
  * "WAF is based on rules from the ```OWASP core rule sets 3.0 or 2.2.9. It automatically updates to include protection against new vulnerabilities, with no additional configuration needed.```"
    * https://www.owasp.org/index.php/Category:OWASP_ModSecurity_Core_Rule_Set_Project 
  * "Monitor your web application against attacks using a real-time WAF log. This log is integrated with Azure Monitor to track WAF alerts and logs and easily monitor trends."
  * "
    SQL injection protection
    Cross site scripting protection
    Common Web Attacks Protection such as command injection, HTTP request smuggling, HTTP response splitting, and remote file inclusion attack
    Protection against HTTP protocol violations
    Protection against HTTP protocol anomalies such as missing host user-agent and accept headers
    Prevention against bots, crawlers, and scanners
    Detection of common application misconfigurations (for example, Apache, IIS, and so on)

* [Enable web application firewall using Azure PowerShell](https://docs.microsoft.com/en-us/azure/application-gateway/tutorial-restrict-web-traffic-powershell)

* [Customize web application firewall rules through the Azure portal](https://docs.microsoft.com/en-us/azure/application-gateway/application-gateway-customize-waf-rules-portal)

* [List of web application firewall CRS rule groups and rules offered](https://docs.microsoft.com/en-us/azure/application-gateway/application-gateway-crs-rulegroups-rules)

* [Web application firewall request size limits and exclusion lists](https://docs.microsoft.com/en-us/azure/application-gateway/application-gateway-waf-configuration)

* [Autoscaling and Zone-redundant Application Gateway (Public Preview)](https://docs.microsoft.com/en-us/azure/application-gateway/application-gateway-autoscaling-zone-redundant)
  * "The autoscaling and zone-redundant application gateway SKU is currently in public preview."


### Articles of possible interest...
* 2018
  * [2018-08-xx zure Application Gateway: monitoring with Log Analytics](http://francescomolfese.it/en/2018/07/azure-application-gateway-come-monitorarlo-con-log-analytics/)
* 2017
  * [2017-04-14 Understanding an Azure Application Gateway with WAF](https://developer.rackspace.com/blog/Azure-WAF-RMS/)
  * [2017-03-30 Azure Web Application Firewall (WAF) Generally Available](https://azure.microsoft.com/sv-se/blog/azure-web-application-firewall-waf-generally-available/)


