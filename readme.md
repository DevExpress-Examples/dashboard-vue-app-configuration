<!-- default badges list -->
![](https://img.shields.io/endpoint?url=https://codecentral.devexpress.com/api/v1/VersionRange/329943881/21.2.4%2B)
[![](https://img.shields.io/badge/Open_in_DevExpress_Support_Center-FF7200?style=flat-square&logo=DevExpress&logoColor=white)](https://supportcenter.devexpress.com/ticket/details/T966015)
[![](https://img.shields.io/badge/📖_How_to_use_DevExpress_Examples-e9f6fc?style=flat-square)](https://docs.devexpress.com/GeneralInformation/403183)
<!-- default badges end -->

## Dashboard for Vue - Configuration

This example shows how you can configure the `DashboardControl` component in a Vue application.

The following properties specify the currently displayed dashboard and designer availability:

- [dashboardId](https://docs.devexpress.com/Dashboard/js-DevExpress.Dashboard.DashboardControlOptions?v=20.2#js_devexpress_dashboard_dashboardcontroloptions_dashboardid)
- [workingMode](https://docs.devexpress.com/Dashboard/js-DevExpress.Dashboard.DashboardControlOptions?v=20.2#js_devexpress_dashboard_dashboardcontroloptions_workingmode)

In addition, the [onBeforeRender](https://docs.devexpress.com/Dashboard/js-DevExpress.Dashboard.DashboardControlOptions?v=20.2#js_devexpress_dashboard_dashboardcontroloptions_onbeforerender) event handler registers the extension that [enables Text Editor functionality](https://docs.devexpress.com/Dashboard/401572/web-dashboard/create-dashboards-on-the-web/designing-dashboard-items/text-box/enable-text-editor-functionality).

See the following file for implementation details:

- [App.vue](./dashboard-vue-app/src/App.vue)

The example uses a client-server architecture. The server (backend) project communicates with the client (frontend) application that includes all the necessary styles, scripts and HTML templates. Note that the script version on the client must match the version of libraries on the server.

- The [asp-net-core-server](asp-net-core-server) folder contains the backend project built with ASP.NET Core 3.1.
- The [dashboard-vue-app](dashboard-vue-app) folder contains the client application built with Vue.

## Quick Start

### Server

In the **asp-net-core-server** folder, run the following command:

```
dotnet run
```

The server starts at `http://localhost:5000` and the client gets data from `http://localhost:5000/api/dashboard`. To debug the server, run the **asp-net-core-server** application in Visual Studio and change the client's `endpoint` property according to the listening port: `https://localhost:44382/api/dashboard`.

See the following section for information on how to install NuGet packages from the DevExpress NuGet feed: [Install DevExpress Controls Using NuGet Packages](https://docs.devexpress.com/GeneralInformation/115912/installation/install-devexpress-controls-using-nuget-packages).

> This server allows CORS requests from _all_ origins with _any_ scheme (http or https). This default configuration is insecure: any website can make cross-origin requests to the app. We recommend that you specify the client application's URL to prohibit other clients from accessing sensitive information stored on the server. Learn more: [Cross-Origin Resource Sharing (CORS)](https://docs.devexpress.com/Dashboard/400709)

### Client

In the **dashboard-vue-app** folder, run the following commands:

```
npm install
npm run serve
```

Open ```http://localhost:8080/``` in your browser to see the result.

## Documentation

- [Create a Vue Dashboard Application](https://docs.devexpress.com/Dashboard/402495/get-started/build-web-dashboard-applications/create-a-vue-dashboard-application)
- [Dashboard Component for Vue](https://docs.devexpress.com/Dashboard/401150/web-dashboard/dashboard-component-for-vue)
- [Install DevExpress Controls Using NuGet Packages](https://docs.devexpress.com/GeneralInformation/115912/installation/install-devexpress-controls-using-nuget-packages)
- 
## Examples

- [Dashboard Component for Angular - Configuration](https://github.com/DevExpress-Examples/dashboard-angular-app-configuration)
- [Dashboard Component for React - Configuration](https://github.com/DevExpress-Examples/dashboard-react-app-configuration)
- [Get Started - Client-Side Dashboard Application (Vue)](https://github.com/DevExpress-Examples/dashboard-vue-app-get-started)
- [ASP.NET Core 3.1 backend for Web Dashboard](https://github.com/DevExpress-Examples/asp-net-core-dashboard-backend)
