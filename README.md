# Google-Summer-of-Code-2022-Work-Product

## Project Details : 

#### Organization : [The Palisadoes Foundation](https://github.com/PalisadoesFoundation/)
#### Project Name : Admin Web Portal: Plugin Architecture 
#### Problem Statement : Latent features in the mobile app should be enabled by installing plugins via the Admin web portal. The API would need to detect the existence of a plugin, and automatically query the plugin for authorization to do some action. When authorized, the mobile app will display new capabilities. This project has two parts:
#### i. The design and development of the plugin architecture

#### ii. The creation of a donations plugin to prove the concept



## Issue and Pull requests :

## 1. Design and devlopement of the plugin architecture.
  The plugin in talawa application  works just like a browser extension works in a browser. The difference here is that the plugin store from which the plugin is installed is handled by the admin of that organization and are used by the members of the organization.
  
 ### Talawa Admin
 
 #### Issue : [Feature Request : [Features as Plugins] Implement UI for AddOnStore with Proper Server Calls](https://github.com/PalisadoesFoundation/talawa-admin/issues/356)
 
 #### Pull request: [Plugin Architecture for Admin](https://github.com/PalisadoesFoundation/talawa-admin/pull/355)
 
 Summary : 
- Refractored Store UI 
- Implement Search Functionality for plugins
- Added fallback screen for the plugin store

 
 
 ### Talawa

 #### Issue : [Feature Request : Plugin Architecture (Features as Plugins)](https://github.com/PalisadoesFoundation/talawa/issues/1339)
 
 #### Pull request: [ [GSoC] Feature Request : Plugin Architecture (Features as Plugins)](https://github.com/PalisadoesFoundation/talawa/pull/1340)
 
 Summary : 
- Implemented `TalawaPluginProvider` widget to implement plugin.
- `fetch_plugin_list` function to load new plugins
- Integrated Plugin list with the Hive database.

 
 
 ### Talawa API

#### Issue : [Feature Request : [Feature Request : [Implementing features as plugins] Implement GraphQL queries and Mutations for Plugin Architecture](https://github.com/PalisadoesFoundation/talawa-api/issues/731)
 
 #### Pull request: [ [GSoC][Feature Request] : Plugin Architecture for Server](https://github.com/PalisadoesFoundation/talawa-api/pull/730)
 
 Summary : 
- Create new MongoDB Model for plugin
- Implemented GraphQL query to get list of plugins `getPlugins`
- Added GraphQL mutation to add new plugin in database `createPlugin`
- Added GraphQL mutation to update install staatus of the plugin for a specific organization `updatePluginStatus`
- Added GraphQL mutation to update the installed organizations list of plugin `updatePluginInstalledOrgs`

 
 ## 2. The creation of Donations plugin to prove the concept
  Donation is a feature on `talawa` mobile app that enables organization members to donate to current organization throught credit card.The Donation is also implemented as plugin which makes it accessible in the mobile app only if it is installed by the admin of that organization
  

### Talawa

#### Issue : [Feature Request : Enabling Plugins , Donation as a Plugin, Refractor for TalawaPluginProvider Widget](https://github.com/PalisadoesFoundation/talawa/issues/1346)
 
 #### Pull request: [ [GSoC][Feature Request] : Enabling Plugins , Donation as a Plugin, Refractor for TalawaPluginProvider Widget ](https://github.com/PalisadoesFoundation/talawa/pull/1355)
 
 Summary : 
- Implementation of Donation feature as a plugin
- Designed and Added Logic to implement Navbar Features a plugins
- Added `TalawaPluginProviderNav` which is used for wrapping the navbar items to make them plugins
- Fixed how the components were rendering using `TalawaPluginProvider`

### Talawa API
