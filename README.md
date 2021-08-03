## Comandos do projeto:

Instalar pacotes: `npm install`. Caso tenha problema na instalação e possívelmente no node-sass, apague o node_modules, rode: `sudo npm install --unsafe-perm node-sass`, e instale novamente os pacotes.

Rodar projeto: `npm serve`.

## Documentation

Documentação do template: [vue argon template](https://www.creative-tim.com/learning-lab/bootstrap-vue/colors/argon-dashboard).

Documentação do boostrap vue: [bootstrap-vue](https://bootstrap-vue.org/)

## Strutura das pastas

```
|-- BootstrapVue Argon Dashboard
    |-- .gitignore
    |-- CHANGELOG.md
    |-- ISSUES_TEMPLATE.md
    |-- LICENSE.md
    |-- README.md
    |-- babel.config.js
    |-- package.json
    |-- public
    |   |-- img
    |   |-- favicon.ico
    |   |-- index.html
    |-- src
        |-- assets
        |   |-- logo.png
        |   |-- scss
        |   |   |-- core
        |   |   |-- custom
        |   |   |-- argon.scss
        |   |-- vendor
        |       |-- nucleo
        |-- components
        |   |-- Badge.vue
        |   |-- BaseAlert.vue
        |   |-- BaseButton.vue
        |   |-- BaseDropdown.vue
        |   |-- BaseHeader.vue
        |   |-- BasePagination.vue
        |   |-- BaseProgress.vue
        |   |-- BaseSlider.vue
        |   |-- BaseTable.vue
        |   |-- ButtonCheckbox.vue
        |   |-- ButtonRadioGroup.vue
        |   |-- CloseButton.vue
        |   |-- index.js
        |   |-- LoadingPanel.vue
        |   |-- Modal.vue
        |   |-- NavbarToggleButton.vue
        |   |-- Breadcrumb
        |   |   |-- Breadcrumb.vue
        |   |   |-- BreadcrumbItem.vue
        |   |   |-- RouteBreadcrumb.vue
        |   |-- Cards
        |   |   |-- Card.vue
        |   |   |-- StatsCard.vue
        |   |-- Charts
        |   |   |-- BarChart.js
        |   |   |-- config.js
        |   |   |-- globalOptionsMixin.js
        |   |   |-- LineChart.js
        |   |   |-- optionHelpers.js
        |   |   |-- roundedCornersExtension.js
        |   |-- Collapse
        |   |   |-- Collapse.vue
        |   |   |-- CollapseItem.vue
        |   |-- Inputs
        |   |   |-- BaseCheckbox.vue
        |   |   |-- BaseInput.vue
        |   |   |-- BaseRadio.vue
        |   |-- Navbar
        |   |   |-- BaseNav.vue
        |   |   |-- NavbarToggleButton.vue
        |   |-- NotificationPlugin
        |   |   |-- index.js
        |   |   |-- Notification.vue
        |   |   |-- Notifications.vue
        |   |-- SidebarPlugin
        |   |   |-- index.js
        |   |   |-- SideBar.vue
        |   |   |-- SidebarItem.vue
        |   |-- Tabs
        |   |   |-- Tab.vue
        |   |   |-- Tabs.vue
        |-- directives
        |   |-- click-ouside.js
        |-- plugins
        |   |-- dashboard-plugin.js
        |   |-- globalComponents.js
        |   |-- globalDirectives.js
        |-- routes
        |   |-- router.js
        |   |-- routes.js
        |   |-- starterRouter.js
        |-- util
        |   |-- throttle.js
        |-- views
            |-- Dashboard.vue
            |-- GoogleMaps.vue
            |-- Icons.vue
            |-- NotFoundPage.vue
            |-- RegularTables.vue
            |-- Dashboard
            |   |-- PageVisitsTable.vue
            |   |-- SocialTrafficTable.vue
            |-- Layout
            |   |-- Content.vue
            |   |-- ContentFooter.vue
            |   |-- DashboardLayout.vue
            |   |-- DashboardNavbar.vue
            |-- Maps
                |-- APY_KEY.js
            |-- Pages
                |-- UserProfile
                |-- AuthLayout.vue
                |-- Login.vue
                |-- Register.vue
                |-- UserProfile.vue
            |-- Starter
                |-- SampleFooter.vue
                |-- SampleLayout.vue
                |-- SampleNavbar.vue
                |-- SamplePage.vue
            |-- Tables
                |-- RegularTables
                |-- projects.js
                |-- users.js
        |-- App.vue
        |-- main.js
        |-- polyfills.js


```

## Navegadores suportados

<img src="https://github.com/creativetimofficial/public-assets/blob/master/logos/chrome-logo.png?raw=true" width="64" height="64"> <img src="https://raw.githubusercontent.com/creativetimofficial/public-assets/master/logos/firefox-logo.png" width="64" height="64"> <img src="https://raw.githubusercontent.com/creativetimofficial/public-assets/master/logos/edge-logo.png" width="64" height="64"> <img src="https://raw.githubusercontent.com/creativetimofficial/public-assets/master/logos/safari-logo.png" width="64" height="64"> <img src="https://raw.githubusercontent.com/creativetimofficial/public-assets/master/logos/opera-logo.png" width="64" height="64">
