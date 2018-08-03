# Modernization Framework release notes

## [Beta release - version 0.1.1808.0]

### How to get and use

#### How to get

- Get binaries via nuget: https://www.nuget.org/packages/SharePointPnPModernizationOnline. You can rename the .nupkg package to .zip and extract the binaries from it
- Optionally self-service compile the binaries by pulling down the https://github.com/SharePoint/PnP-Tools/tree/master/Solutions/SharePoint.Modernization/SharePointPnP.Modernization.Framework project from GitHub

#### How to use

- From .Net: see https://github.com/SharePoint/PnP/tree/dev/Samples/Modernization.PageTransformation as nice sample to start with
- From PnP PowerShell: see https://github.com/SharePoint/PnP-Tools/blob/master/Solutions/SharePoint.Modernization/Scripts/PageTransformation/TransformPageSample.ps1 for a sample


### Added

- Header (H1 to H4) alignment is retained when transforming wiki text
- Combined styles (e.g. forecolor with strike-through and font size) are now correctly handled when transforming wiki text
- Documentation for functions and selectors is now autogenerated (https://docs.microsoft.com/en-us/sharepoint/dev/transform/modernize-userinterface-site-pages-api)
- Support added for having text before and after the web part but inside the div surrounding the web part
- Theme colors are transformed now
- Source page item level permissions are copied to the target page (can be optionally turned off)

### Changed

- Page title handling got improved
- Improved handing of BR tags
- Improved reliability in handling image URL's outside of the current web
- Fixed layout transformation for HeaderRightColumnBody and HeaderLeftColumnBody web part page layouts
- Fixed "duplicate key" issue when transforming multiple pages in sequence
- Fixed ListId datatype in model
- Calendar is now transformed to the Events web part
- Tasks web part is not transformed anymore
- Correctly identify a discussion board