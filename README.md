# IdentityInt

Basic Test project for https://github.com/aspnet/Docs/issues/6784

just created an  ASP.NET MVC Core2.1 web site, and followed https://github.com/aspnet/Docs/issues/6784

Recreated the initial Migration.

Exception :
Microsoft.AspNetCore.Mvc.Internal.ControllerActionInvoker:Information: Executed action IdentityInt.Controllers.HomeController.Index (IdentityInt) in 252.6203ms
'dotnet.exe' (CoreCLR: clrhost): Loaded 'C:\Program Files\dotnet\shared\Microsoft.NETCore.App\2.1.0\System.Diagnostics.StackTrace.dll'. Skipped loading symbols. Module is optimized and the debugger option 'Just My Code' is enabled.
'dotnet.exe' (CoreCLR: clrhost): Loaded 'C:\Program Files\dotnet\shared\Microsoft.NETCore.App\2.1.0\System.Reflection.Metadata.dll'. Skipped loading symbols. Module is optimized and the debugger option 'Just My Code' is enabled.
Microsoft.AspNetCore.Diagnostics.DeveloperExceptionPageMiddleware:Error: An unhandled exception has occurred while executing the request.

System.InvalidOperationException: No service for type 'Microsoft.AspNetCore.Identity.UserManager`1[Microsoft.AspNetCore.Identity.IdentityUser]' has been registered.
   at Microsoft.Extensions.DependencyInjection.ServiceProviderServiceExtensions.GetRequiredService(IServiceProvider provider, Type serviceType)
   at Microsoft.AspNetCore.Mvc.Razor.Internal.RazorPagePropertyActivator.<>c__DisplayClass8_0.<CreateActivateInfo>b__1(ViewContext context)
   at Microsoft.Extensions.Internal.PropertyActivator`1.Activate(Object instance, TContext context)
   at Microsoft.AspNetCore.Mvc.Razor.Internal.RazorPagePropertyActivator.Activate(Object page, ViewContext context)
   at Microsoft.AspNetCore.Mvc.Razor.RazorPageActivator.Activate(IRazorPage page, ViewContext context)
   at Microsoft.AspNetCore.Mvc.Razor.RazorView.RenderPageCoreAsync(IRazorPage page, ViewContext context)
   at Microsoft.AspNetCore.Mvc.Razor.RazorView.RenderPageAsync(IRazorPage page, ViewContext context, Boolean invokeViewStarts)
   at Microsoft.AspNetCore.Mvc.Razor.RazorView.RenderAsync(ViewContext context)
   at Microsoft.AspNetCore.Mvc.TagHelpers.PartialTagHelper.RenderPartialViewAsync(TextWriter writer, Object model)
   at Microsoft.AspNetCore.Mvc.TagHelpers.PartialTagHelper.ProcessAsync(TagHelperContext context, TagHelperOutput output)
   at Microsoft.AspNetCore.Razor.Runtime.TagHelpers.TagHelperRunner.RunAsync(TagHelperExecutionContext executionContext)
   at AspNetCore.Views_Shared__Layout.<ExecuteAsync>b__46_1()
   at Microsoft.AspNetCore.Razor.Runtime.TagHelpers.TagHelperExecutionContext.SetOutputContentAsync()
   at AspNetCore.Views_Shared__Layout.ExecuteAsync()
   at Microsoft.AspNetCore.Mvc.Razor.RazorView.RenderPageCoreAsync(IRazorPage page, ViewContext context)
   at Microsoft.AspNetCore.Mvc.Razor.RazorView.RenderPageAsync(IRazorPage page, ViewContext context, Boolean invokeViewStarts)
   at Microsoft.AspNetCore.Mvc.Razor.RazorView.RenderLayoutAsync(ViewContext context, ViewBufferTextWriter bodyWriter)
   at Microsoft.AspNetCore.Mvc.Razor.RazorView.RenderAsync(ViewContext context)
   at Microsoft.AspNetCore.Mvc.ViewFeatures.ViewExecutor.ExecuteAsync(ViewContext viewContext, String contentType, Nullable`1 statusCode)
   at Microsoft.AspNetCore.Mvc.ViewFeatures.ViewExecutor.ExecuteAsync(ActionContext actionContext, IView view, ViewDataDictionary viewData, ITempDataDictionary tempData, String contentType, Nullable`1 statusCode)
   at Microsoft.AspNetCore.Mvc.ViewFeatures.ViewResultExecutor.ExecuteAsync(ActionContext context, ViewResult result)
   at Microsoft.AspNetCore.Mvc.ViewResult.ExecuteResultAsync(ActionContext context)
   at Microsoft.AspNetCore.Mvc.Internal.ResourceInvoker.InvokeResultAsync(IActionResult result)
   at Microsoft.AspNetCore.Mvc.Internal.ResourceInvoker.InvokeNextResultFilterAsync[TFilter,TFilterAsync]()
   at Microsoft.AspNetCore.Mvc.Internal.ResourceInvoker.Rethrow(ResultExecutedContext context)
   at Microsoft.AspNetCore.Mvc.Internal.ResourceInvoker.ResultNext[TFilter,TFilterAsync](State& next, Scope& scope, Object& state, Boolean& isCompleted)
   at Microsoft.AspNetCore.Mvc.Internal.ResourceInvoker.InvokeResultFilters()
   at Microsoft.AspNetCore.Mvc.Internal.ResourceInvoker.InvokeNextResourceFilter()
   at Microsoft.AspNetCore.Mvc.Internal.ResourceInvoker.Rethrow(ResourceExecutedContext context)
   at Microsoft.AspNetCore.Mvc.Internal.ResourceInvoker.Next(State& next, Scope& scope, Object& state, Boolean& isCompleted)
   at Microsoft.AspNetCore.Mvc.Internal.ResourceInvoker.InvokeFilterPipelineAsync()
   at Microsoft.AspNetCore.Mvc.Internal.ResourceInvoker.InvokeAsync()
   at Microsoft.AspNetCore.Builder.RouterMiddleware.Invoke(HttpContext httpContext)
   at Microsoft.AspNetCore.Authentication.AuthenticationMiddleware.Invoke(HttpContext context)
   at Microsoft.AspNetCore.StaticFiles.StaticFileMiddleware.Invoke(HttpContext context)
   at Microsoft.AspNetCore.Diagnostics.EntityFrameworkCore.MigrationsEndPointMiddleware.Invoke(HttpContext context)
   at Microsoft.AspNetCore.Diagnostics.EntityFrameworkCore.DatabaseErrorPageMiddleware.Invoke(HttpContext httpContext)
   at Microsoft.AspNetCore.Diagnostics.EntityFrameworkCore.DatabaseErrorPageMiddleware.Invoke(HttpContext httpContext)
   at Microsoft.AspNetCore.Diagnostics.DeveloperExceptionPageMiddleware.Invoke(HttpContext context)
