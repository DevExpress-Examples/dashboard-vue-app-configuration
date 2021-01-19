# Dashboard Vue Example

This example is a ready-to-use client Vue application with the DevExpress Dashboard component.

This example illustrates how to use the Vue-based `DashboardControl` component for displaying and editing dashboards. The following properties are used to switch the working mode and the currently displayed dashboard: 

- [workingMode](https://docs.devexpress.com/Dashboard/js-DevExpress.Dashboard.DashboardControlOptions?v=20.2#js_devexpress_dashboard_dashboardcontroloptions_workingmode)
- [dashboardId](https://docs.devexpress.com/Dashboard/js-DevExpress.Dashboard.DashboardControlOptions?v=20.2#js_devexpress_dashboard_dashboardcontroloptions_dashboardid)

In addition, the example shows how to use the [onBeforeRender](https://docs.devexpress.com/Dashboard/js-DevExpress.Dashboard.DashboardControlOptions?v=20.2#js_devexpress_dashboard_dashboardcontroloptions_onbeforerender) event to [Enable Text Editor Functionality](https://docs.devexpress.com/Dashboard/401572/web-dashboard/create-dashboards-on-the-web/designing-dashboard-items/text-box/enable-text-editor-functionality) in code. 

See the following file for implementation details:

- [App.vue](./dashboard-vue-app/src/App.vue)

The example uses a modular approach that based on the client-server model. You need a server (backend) project and a client (frontend) application that includes all the necessary styles, scripts and HTML-templates. Note that the script version on the client should match with libraries version on the server up to a minor version.

- The [asp-net-core-server](asp-net-core-server) folder contains an ASP.NET Core 3.1 Dashboard application.
- The [dashboard-vue-app](dashboard-vue-app) folder contains a client application.

## Quick Start

In the **asp-net-core-server** folder, run the following command:

```
dotnet run
```
> This server allows CORS requests from _all_ origins with _any_ scheme (http or https). It is insecure, because any website can make cross-origin requests to the app. We recommend you specify the client application's URL directly to prohibit clients from getting access to your personal information on your server. Learn more: [Cross-Origin Resource Sharing (CORS)](https://docs.devexpress.com/Dashboard/400709)

In the **dashboard-vue-app** folder, run the following command:

```
npm run serve
```

Open ```http://localhost:8080/``` in your browser to see the result.

## Documentation
- [Add Web Dashboard to a Vue Application](https://docs.devexpress.com/Dashboard/402486/web-dashboard/dashboard-component-for-vue/add-web-dashboard-to-a-vue-application?v=20.2)
- [Dashboard Component for Vue](https://docs.devexpress.com/Dashboard/401150/web-dashboard/dashboard-component-for-vue?v=20.2)

## Examples
- [Dashboard Client-Side Application (Vue)](https://github.com/DevExpress-Examples/dashboard-vue-app)
- [Dashboard Client-Side Application (React)](https://github.com/DevExpress-Examples/dashboard-react-app)
- [Dashboard Client-Side Application (Angular)](https://github.com/DevExpress-Examples/dashboard-angular-app)
- [ASP.NET Core 3.1 backend for Web Dashboard](https://github.com/DevExpress-Examples/asp-net-core-dashboard-backend)
