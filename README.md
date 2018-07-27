# WebAPI with Swagger and Help pages

1. Craete Web API project Template
2. Install Swagger with command Install-Package Swashbuckle -Version 5.6.0
3. Navigate to http://localhost:58554/swagger/ui/index will get swagger
4. Install help pages with the command Install-Package Microsoft.AspNet.WebApi.HelpPage
5. Add the following code in Application_Start
    AreaRegistration.RegisterAllAreas();
6. To enable this feature, open the file Areas/HelpPage/App_Start/HelpPageConfig.cs and uncomment the following line

config.SetDocumentationProvider(new XmlDocumentationProvider(
    HttpContext.Current.Server.MapPath("~/App_Data/XmlDocument.xml")));

7. In project properties under Output check XML documentation file and add App_Data/XmlDocument.xml.

8. Navigate to http://localhost:58554/help/index to get the help page.


