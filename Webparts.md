# Web part / Solutions  / SPFX Review
If you are still using WSP files it's time to start looking at rewriting those into [SPFX]
(https://docs.microsoft.com/en-us/sharepoint/dev/spfx/sharepoint-framework-overview).

from SharePoint Server 2016  onwards this is supported. See [Supported extensibility platforms - overview](https://docs.microsoft.com/en-us/sharepoint/dev/spfx/supported-extensibility-platforms-overview)


## Security Review

The MCSA code review tool was retired on 1st March 2022 [Microsoft Security Code Analysis – a tool that seamlessly empowers customers to enable security controls in your CI/CD pipeline -Blog Post](https://devblogs.microsoft.com/premier-developer/microsoft-security-code-analysis/)

Please refer to the [OWASP Source Code Analysis Tools](https://owasp.org/www-community/Source_Code_Analysis_Tools) for alternative options in Azure DevOps. 
 Consider implementing  tools such as [HCL AppScan CodeSweep - GitHub Action](https://hclsw.co/codesweepgithub) which supports JS (Vue, React, Node, Angular, JQuery) or  [Solar Lint](https://www.sonarlint.org/).

 SonarLint is a Free and Open Source IDE extension that identifies and helps you fix quality and security issues as you code.

There is also a very helpful [blog](https://helloitsliam.com/2018/07/04/security-scanning-a-sharepoint-framework-solution/) explaining all the options here.

For customers planning to migrate to GitHub, you can check out [GitHub Advanced Security](https://docs.github.com/github/getting-started-with-github/about-github-advanced-security).

* Share the build folder with the security team to scan.
* You should also do a peer review of your code.


## Update process

