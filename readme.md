# Dashboard Component for Vue - Configuration

This example illustrates how to configure the Vue-based `DashboardControl` component. The following properties are used to switch the working mode and the currently displayed dashboard:

- [workingMode](https://docs.devexpress.com/Dashboard/js-DevExpress.Dashboard.DashboardControlOptions?v=20.2#js_devexpress_dashboard_dashboardcontroloptions_workingmode)
- [dashboardId](https://docs.devexpress.com/Dashboard/js-DevExpress.Dashboard.DashboardControlOptions?v=20.2#js_devexpress_dashboard_dashboardcontroloptions_dashboardid)

In addition, the example shows how to handle the [onBeforeRender](https://docs.devexpress.com/Dashboard/js-DevExpress.Dashboard.DashboardControlOptions?v=20.2#js_devexpress_dashboard_dashboardcontroloptions_onbeforerender) event and [enable Text Editor functionality](https://docs.devexpress.com/Dashboard/401572/web-dashboard/create-dashboards-on-the-web/designing-dashboard-items/text-box/enable-text-editor-functionality) in code.

See the following file for implementation details:

- [App.vue](./dashboard-vue-app/src/App.vue)

The example uses a modular approach that based on the client-server model. You need a server (backend) project and a client (frontend) application that includes all the necessary styles, scripts and HTML-templates. Note that the script version on the client should match with libraries version on the server.

- The [asp-net-core-server](asp-net-core-server) folder contains the backend project built with ASP.NET Core 3.1.
- The [dashboard-vue-app](dashboard-vue-app) folder contains the client application built with Vue.

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

- [Create a Vue Dashboard Application](https://docs.devexpress.com/Dashboard/402495/get-started/build-web-dashboard-applications/create-a-vue-dashboard-application?v=20.2)
- [Dashboard Component for Vue](https://docs.devexpress.com/Dashboard/401150/web-dashboard/dashboard-component-for-vue?v=20.2)

## Examples

- [Dashboard Component for Angular - Configuration](https://github.com/DevExpress-Examples/dashboard-angular-example)
- [Dashboard Component for React - Configuration](https://github.com/DevExpress-Examples/dashboard-react-example)
- [Get Started - Client-Side Dashboard Application (Vue)](https://github.com/DevExpress-Examples/dashboard-vue-app)
- [ASP.NET Core 3.1 backend for Web Dashboard](https://github.com/DevExpress-Examples/asp-net-core-dashboard-backend)
