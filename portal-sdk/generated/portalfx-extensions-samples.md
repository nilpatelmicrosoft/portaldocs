<a name="portal-extension-samples"></a>
# Portal Extension Samples

 ## Overview

One of the most productive ways to learn how to develop code is by reviewing program source.  The Azure portal team ships samples that extension developers can leverage.

All developers who install the Portal Framework SDK that is located at [http://aka.ms/portalfx/download](http://aka.ms/portalfx/download) also install the samples on their computers during the installation the process. The samples are located in the `...\Documents\PortalSDK\FrameworkPortal\Extensions\SamplesExtension` folder.

First-party extension developers, i.e. Microsoft employees, have access to the Dogfood environment, therefore they can view the samples that are located at [http://aka.ms/portalfx/samples#blade/SamplesExtension/SDKBlade](http://aka.ms/portalfx/samples#blade/SamplesExtension/SDKBlade).

<a name="portal-extension-samples-samples-extension"></a>
## Samples extension

The samples extension provides an individual sample for each feature available in the framework, as described in the following image.

 ![alt-text](../media/portalfx-extensions-samples/samples.png  "Samples Extension Solution")

After installing the Portal Framework SDK, the local instance of the portal will open with the samples extension pre-registered.  You can open the `SamplesExtension` solution file to experiment with samples in the IDE.

```bash
[My Documents]\PortalSDK\FrameworkPortal\Extensions\SamplesExtension\SamplesExtension.sln
```

The samples and the portal can be located with **IntelliMirror** in the following location.

```bash
%LOCALAPPDATA%\PortalSDK\FrameworkPortal\Extensions\SamplesExtension\SamplesExtension.sln
```

You can edit the samples and then refresh the portal to see the changes. Each sample demonstrates a single usage of the API.  It is great for detailed information on any one API.

For help other than documentation and samples, send an email to the Ibiza team on [Stackoverflow@MS](https://stackoverflow.microsoft.com/questions/tagged?tagnames=ibiza). For a list of topics and stackoverflow tags, see [portalfx-extensions-stackoverflow.md](portalfx-extensions-stackoverflow.md).

<!-- TODO: Determine whether there should be a list of samples and whether they are V1 or V2.   
The alternative is to let the list default to the contents of the SamplesExtension.sln project. -->

<a name="portal-extension-samples-v1-versus-v2"></a>
## V1 versus V2

The samples are structured into two directories, **V1** and **V2**, as in the following example. 

 ![alt-text](../media/portalfx-extensions-samples/v1-and-v2.png  "V1 and V2 Directories")

<!--TODO: Can "meant" be changed to "will"  or "intended" ? -->

<a name="portal-extension-samples-v1-versus-v2-v2"></a>
### V2

The samples in the **V2** directories use the latest patterns. It contains the post-GA collection of new APIs that are meant to be the only set of APIs needed to develop an Ibiza extension.

The **V2** samples address the following API areas.

* New Blade variations TemplateBlade, FrameBlade, MenuBlade 

* Blade-opening/closing `container.openBlade`, et al

* no-PDL TypeScript decorators that define all recommended Blade/Part variations

* Forms that do not use **V1** EditScope. For more information about EditScope, see [portalfx-forms-edit-scope-faq.md](portalfx-forms-edit-scope-faq.md).

<a name="portal-extension-samples-v1-versus-v2-v1"></a>
### V1

Our **V1** APIs use APIs that support previous UX patterns, or  are becoming obsolete or are less commonly used.  The **V1** APIs are also more difficult to use than the new API, for both the UX design and  the associated APIs.

The following **V1** concepts should be avoided when **V2** APIs can be used instead.

* PDL
* EditScope
* ParameterCollector/ParameterProvider
* Blades containing Parts
* Non-full-screen Blades, i.e., ones that open with a fixed width
* **V1** Blade-opening -- Selectable/SelectableSet APIs
* **V1** Forms that use EditScope

**NOTE**: The **V2** space is not yet entirely built. In the meantime, use **V1** APIs in places, even the previously-listed **V1** concepts. For example, the source code for small, medium, and large blades is located in the `...\SamplesExtension\Extension\Client\V1\Blades\BladeWidth` directory.

 ## Procedures for Portal Sample Source Code

After installing Visual Studio and the Portal Framework SDK, locate the samples in the `...\Documents\PortalSDK\FrameworkPortal\Extensions\SamplesExtension` folder.

Open the `SamplesExtension` solution file to experiment with samples in the IDE.

You can make changes to the samples as appropriate.

Click the F5 key to start debugging the sample extensions. This rebuilds the project, which will allow you to check for items like the most recent version of the SDK.

Sideload the extension. When it loads, click on the `More Services` option in the menu, as in the following example.

 ![alt-text](../media/portalfx-extensions-samples/samples-services.png  "Portal Extensions Services")

In the filter box, search for "Azure Portal SDK". You can use `Shift + Space` to mark it as a favorite site.

Make changes to the sample that best fits the needs of the development project, then refresh the portal to view the changes. 


 ## Glossary

This section contains a glossary of terms and acronyms that are used in this document. For common computing terms, see [https://techterms.com/](https://techterms.com/). For common acronyms, see [https://www.acronymfinder.com](https://www.acronymfinder.com).

| Term                  | Meaning | 
| ---                   | --- |
| EditScope             | An Azure SDK object that provides a standard way of managing edits over a collection of input fields, blades, and extensions. |
| ParameterCollector    | A collection of Parameter and Parameter-derived objects that are used by data source controls in advanced data-binding scenarios. |