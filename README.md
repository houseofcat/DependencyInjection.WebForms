# HouseofCat.DependencyInjection.WebForms
 Dependency Injection for Asp.Net WebForms (currently only Unity)

## How to use
1. Make sure your web project is targeting .NET Framework 4.8. You can download .NET Framework 4.8 developer pack from [here](https://www.microsoft.com/net/download/thank-you/net48-developer-pack). Check web.config and targetFramework in httpRuntime section should be 4.8.
```xml
<system.web>
  <compilation debug="true" targetFramework="4.8"/>
  <httpRuntime targetFramework="4.8"/>
</system.web>
```
2. Install Microsoft.AspNet.WebFormsDependencyInjection.Unity nupkg in your project.
3. Open Global.asax.cs and register the types in UnityContainer.
```csharp
protected void Application_Start(object sender, EventArgs e)
{
    var container = this.AddUnity();

    container.RegisterType<ISomeInterface, SomeImplementation>();
}
```

## Source
Original Repository no longer maintained by Microsoft is found [here](https://github.com/aspnet/AspNetWebFormsDependencyInjection).
