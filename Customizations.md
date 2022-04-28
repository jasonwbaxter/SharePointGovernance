# Web part / Solutions  / SPFX Review
If you are still using WSP files it's time to start looking at rewriting those into [SPFX](https://docs.microsoft.com/en-us/sharepoint/dev/spfx/sharepoint-framework-overview). 

See the [Migration guidance](https://docs.microsoft.com/en-us/sharepoint/dev/spfx/web-parts/guidance/migrate-script-editor-web-part-customizations) article for more information on replacing traditional methods such as Script Editor ,Jquery ,DataTables etc.

If you are on SharePoint Server 2016 or later this is the preferred and  supported model. 

See [Supported extensibility platforms - overview](https://docs.microsoft.com/en-us/sharepoint/dev/spfx/supported-extensibility-platforms-overview)


## How to do a security review

The MCSA code review tool was retired on 1st March 2022 [Microsoft Security Code Analysis – a tool that seamlessly empowers customers to enable security controls in your CI/CD pipeline -Blog Post](https://devblogs.microsoft.com/premier-developer/microsoft-security-code-analysis/)

Please refer to the [OWASP Source Code Analysis Tools](https://owasp.org/www-community/Source_Code_Analysis_Tools) for alternative options in Azure DevOps. 
 Consider implementing  tools such as [HCL AppScan CodeSweep - GitHub Action](https://hclsw.co/codesweepgithub) which supports JS (Vue, React, Node, Angular, JQuery) or  [Solar Lint](https://www.sonarlint.org/).

 SonarLint is a Free and Open Source IDE extension that identifies and helps you fix quality and security issues as you code.

There is also a very helpful [blog](https://helloitsliam.com/2018/07/04/security-scanning-a-sharepoint-framework-solution/) explaining all the options here.

For customers planning to migrate to GitHub, you can check out [GitHub Advanced Security](https://docs.github.com/github/getting-started-with-github/about-github-advanced-security).

* Share the build folder with the security team to scan.
* You should also do a peer review of your code.


## Update a SPFX project

To find the outdated packages in your client-side project, including SharePoint Framework and other packages your project depends on, run the following command in a console in the same directory as your project.

* Run to get a list of outdated packages
  
   ```
   npm outdated

* install manually each outdated package
  
  ```
    npm install mypackage@newversion --save
    gulp clean


* Delete the folder node_modules
* Run npm install
* Rebuild the solution using gulp build
* Update Yeoman Generator npm outdated -g
* Update the SP Generator npm install @microsoft/generator-sharepoint@latest -g
  
When you run the npm outdated command in a project that targets both SharePoint Online and SharePoint Server 2016, it shows you the latest versions of the SharePoint Framework packages. These versions, however, work only with SharePoint Online. If you update your solution to use these latest packages, it no longer works with SharePoint Server 2016.

Read  how to [setup your development environment](https://docs.microsoft.com/en-us/sharepoint/dev/spfx/set-up-your-development-environment)

|SP Version|SPFX version|Node version|NPM|TypeScript|React|Hyperlink|
|---|---|---|---|---|---|---|
|SharePoint Online|Latest|LTS v12, LTS v14|v5, v6|v3.9|v16.13.1|[link](https://docs.microsoft.com/en-us/sharepoint/dev/spfx/spfx-sharepoint-online)|
|SharePoint Server 2019|v1.4.1|LTS v6, LTS v8|v3, v4|v2.4|v15|[link](https://docs.microsoft.com/en-us/sharepoint/dev/spfx/sharepoint-2019-support)|
|SharePoint Server 2016 SP2| v1.1.0|LTS v6||v3, v4|v2.4|v15|[link](https://docs.microsoft.com/en-us/sharepoint/dev/spfx/sharepoint-2016-support)|

See MS updated pages [here](https://docs.microsoft.com/en-us/sharepoint/dev/spfx/compatibility)