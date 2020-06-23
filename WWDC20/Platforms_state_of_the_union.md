WWDC20

* [Platforms State of the Union](#platforms-state-of-the-union)
      * [Apple Silicon](#apple-silicon)
      * [iPadOS](#ipados)
      * [Widgets](#widgets)
      * [App Clips](#app-clips)
      * [Xcode and API Updates](#xcode-and-api-updates)

# Platforms State of the Union

## Apple Silicon
- New ARM based silicon
- Ship apps with both executables using a new format called Universal 2
- Rosetta 2, an emulation layer that lets you run old apps on new Macs.
    - After an installation of an old app, the Mac will examine the app and try to optimize it for the ARM processor. This way, there will be some level of optimization even before users open the app.
    - Rosetta 2 can also translate instructions from x86 to ARM on the fly, while you’re running the app.
- For code that is going to run on servers, Apple is also working on a set of virtualization tools. Users will be able to run Linux and Docker on an ARM Mac.
- The transition is going to take around two years.

## iPadOS
- Side bars in a three grouped layout
    - UIKit: `UISplitViewController`
    - SwiftUI: `NavigationBar`
    - New outlines built using `List` on SwiftUI and `UICollectionView` on UIKit
- New color picker api
- Depth API 
- PencilKit and the new Canvas API gives the ability to use scribble for textfield input and copy/paste/duplicate features for the handwritten text
- Stroke API gives detail about the handrwriting input

## Widgets
- User interface code is transformed into an 'Arhived View' to perform efficiently on home screen
- Widget API uses "snapshots" of these archived views to show updates for the widget. So the app is not needed to be running in the background all the time.
- `Widget` protocol and `TimelineProvider` 
    - `func snapshot` tells the system when to display anything when needed

## App Clips
- Designed for speed,
- The appearing card from the bottom is autogenerated by Apple as soon as the app is live on the appstore,
- Made from a part of your app,
- Leave out logics like analytics and so on for a lightweight eperience,
- Ability to prompt the user to upgrade and get the full app experience (Storekit overlay),
- New Target -> App Clip.

## Xcode and API Updates
- New StoreKitTest framework
    - Ability to imitate IAP scenarios without needing to deploy,
- 12x faster code completion (Seriously?!?)
- A new enriched swiftUI preview view 
    - Ability to edit the code and content by interacting the sswiftUI preview,
    - Easily duplicate the preview for another device size or dark/light mode
- New tab and folder management just like in browsers,
    - Ability to open whole folder hierarchy in tabs.
- SPM with asset catalog, resource and localization support!!!

- Large, complex collection views with memory efficieny
    - Using `Lazy` components like `VStack` vs `LazyVStack`