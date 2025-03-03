---
banner: https://s3.amazonaws.com/coursera/media/Grid_Coursera_Partners_updated.png
created: 2024-06-17T10:40:04
source: https://www.coursera.org/learn/os-power-user/supplement/Smg89/supplemental-reading-for-windows-software-packages
author: 
cssclasses:
  - dashboard
---

```meta-bind-button
label: Fold All
icon: ""
hidden: false
class: ""
tooltip: ""
id: "001"
style: primary
actions:
  - type: command
    command: editor:fold-all

```

```cardlink
url: https://www.coursera.org/learn/os-power-user/supplement/Smg89/supplemental-reading-for-windows-software-packages
title: "Supplemental Reading for Mobile App Packages | Coursera"
description: "In the third module of this course, we'll learn about package and software management in Windows and Linux OS. It's important to know how package installs work and how devices and drivers are managed within these operating systems. We will also ..."
host: www.coursera.org
image: https://s3.amazonaws.com/coursera/media/Grid_Coursera_Partners_updated.png
```
# Supplemental Reading for Mobile App Packages

# Mobile App Distribution

You are likely familiar with using either the Apple App Store or Google Play store to download and install apps on your smartphone. As an IT Support professional, you may need to deploy mobile apps across large organizations. In this reading, you will learn more about how mobile apps are distributed both publicly and privately for iOS and Android. 

## How apps are distributed

### Apple mobile apps

Apple’s App Store provides apps to millions of mobile devices around the world, including the iPhone, iPad, and Apple Watch. Apple’s App Store Connect allows developers and organizations to distribute both public and private apps, provided that the app passes an intensive review process to meet Apple’s quality standards. App Store Connect also allows developers and organizations to set individualized prices for the apps, enter banking information to accept payments for apps or in-app purchases, schedule beta testing, and more. Apple recommends that developers use the Xcode integrated development environment (IDE) or Ad Hoc for developing iOS, iPadOS, and watchOS apps.

**Apple’s App Store**

Apple’s public App Store is a marketplace that reaches millions of Apple mobile device users across the world. The App Store offers developers unlimited bandwidth for hosting, handles payment processing, verifies users, etc. Developers must first register through the Apple Developer Program if they wish to distribute apps through the App Store. The Apple Developer Program offers resources, tools, and support for app development, including testing tools, beta software, analytics, etc. Apple has a long and detailed list of guidelines for all apps that developers and organizations must follow. The guidelines include rules for safety, third-party software development kits (SDKs), ad networks, trademarks and copyrights, and much more. Additionally, submitted apps cannot be copies of other developers’ products, nor can they be designed to steal users’ data. Though the Apple Store Connect review process is rigorous, the platform also provides an appeals process for rejected apps.

### **Custom Apple apps**

Organizations may opt to create private customized apps to meet specific and unique organizational needs. These custom apps may be designed for the organization’s students, employees, clients, partners, franchisees, etc. Organizations can choose to offer the apps for free, for a price, or through special redemption codes. They also have the option to automatically distribute and configure apps to large numbers of registered devices using Mobile Device Management (MDM).  

Apple offers a couple of options for private and secure customized app distribution:

-   **Apple School Manager** \- For educational institutions, provides the option to distribute proprietary apps for internal use and to purchase other apps in large volumes, often with educator discounts. Common apps in Apple School Manager might include those for course registration or digital textbook access. Apple School Manager also offers educational institutions the ability to create accounts for students and staff, as well as to setup automatic device enrollment.
    
-   **Apple Business Manager** \- For businesses, offers similar features as the Apple School Manager including the distribution and purchase of private apps, as well as the automatic deployment of apps to the business’ mobile devices. As an IT Support professional, you might want to volume purchase mobile virus protection and automatically deploy the app across your business’ mobile devices. An organization can set private audience groups in App Store Connect. The audience groups will be able to see and download the organization’s custom apps through the Apps and Books or Content sections of the Apple School and Apple Business Managers. 
    

**Outside official Apple distribution channels**

Some developers and organizations might not want to use an Apple platform for app distribution. As an alternative, they have the option to distribute Apple “trusted developer” apps from websites or private file shares using their Apple Developer ID certificate and Apple’s notarization process.

### Android mobile apps

Google makes considerable investments into Android development, the Google Play platform, services, tools, and marketing to support developers and organizations who choose Google Play to deploy Android apps. Android Studio is the official Android integrated development environment (IDE) for developing Android apps. Android Studio is used to compile Android Package Kit (APK) files, and the Android App Bundle is used to publish apps to Google Play. The Android App Bundle enables Google Play to automatically generate the APK files for a variety of devices and provide app signing keys. This service is a significant time saver for developers and it ensures Google Play apps will work on most Android devices. 

**Google Play Store**

Google Play revenue makes it possible for Google to offer the open Android operating system for free to device manufacturers in order to promote growth and innovation. This business model has driven Android adoption across 24,000+ device models with **billions** of Android mobile device users around the world. The Google Play store hosts 2 million apps and games with 140+ billion downloads per year, and growing. Google also keeps consumers safe with Google Play’s built-in protections, which require developers to adhere to high safety standards.

To distribute an app publicly through the Google Play Store, a developer will: 

1.  Create a Google Play developer account.
    
2.  Use the Google Play Console to Create App.
    
    1.  Provide preliminary information about the app.
        
    2.  Review and agree to the Developer Program Policies, Terms of Service, and documentation about export laws (where applicable).
        
3.  Use the app’s Dashboard for guidance through the app publishing process:
    
    1.  Google Play Store listing
        
    2.  Pre-release management
        
    3.  Prepare a release
        
    4.  Testing
        
    5.  Submit app and declarations for review by Google
        
    6.  Promotion/pre-registration
        
    7.  Publish app (upon review approval) 
        

**Custom Android Apps**

Large organizations, or Enterprise customers, can use “managed Google Play” as a distribution tool for deploying apps to employees. Enterprise customers operate their own Google Play store to host their apps publicly and/or privately. They can grant access to select users or user groups to view and download private apps. 

Google Play Custom App Publishing API is an Application Programming Interface from Google that enables developers and organizations to create and publish private custom apps. Apps that are published through Google Play Custom App Publishing API cannot be converted to public apps. The apps will remain private permanently. Google offers a streamlined verification process for private custom apps. These apps can be available to an organization for deployment in as little as 5 minutes after verification. 

Google Play Custom App Publishing API can be used by:

-   Enterprise mobility management providers (EMMs)
    
-   Third-party app developers
    
-   Organizations/developers that want their enterprise clients to be able to distribute private/custom apps from an EMM console, IDE, or other interface.
    

Enterprise customers can publish apps by: 

1.  Enabling the Google Play Custom App Publishing API.
    
2.  Creating a service account.
    
3.  Granting publishing permission to the service account on the organization’s Play Console developer account.
    

Using Google Play within an organization, IT Support administrators should:

1.  Use their organization’s managed version of Google Play to select and approve apps.
    
2.  Ensure all employee Android devices are set up to use the organization’s managed Google Play account.
    
3.  Use the organization’s Enterprise Mobility Manager (EMM) to manage employee Android devices and deploy selected apps to employees’ Android devices.
    

For Android devices that are owned by employees (BYODs) and not registered with the organization’s EMM: 

1.  Consider Google’s recommendation to create a work profile on each device.. 
    
2.  Show employees how to use their work profile to access the organization’s managed Google Play account. 
    
3.  Demonstrate that employees can then view and install any of the administrator selected and approved apps. 
    

**Outside official Google distribution channels**

Google’s open platform policies includes allowing competitors to innovate in developing app stores. Some alternative app stores that distribute Android apps include:

-   APKMirror
    
-   Aurora Store
    
-   Aptoide
    
-   Amazon Appstore
    
-   F-Droid
    
-   Uptodown
    
-   SlideMe
    
-   APKPure
    
-   Galaxy Store
    
-   Yalp Store
    

Please see Fossbytes “[10 Best Google Play Store Alternatives: Websites And AppsOpens in a new tab](https://fossbytes.com/10-google-play-store-alternatives/)” for more information about each Android app store in the list above.

## Resources for more information

-   [App Store Review GuidelinesOpens in a new tab](https://developer.apple.com/app-store/review/guidelines/) - Apple’s comprehensive list of guidelines developers must follow for designing and submitting apps to the Apple App Store. 
    
-   [Distributing custom apps for businessOpens in a new tab](https://developer.apple.com/business/custom-apps/) - Apple’s guide to publishing custom apps.
    
-   [About Android App BundlesOpens in a new tab](https://developer.android.com/guide/app-bundle) - Android developer’s guide to using Android App Bundles to develop and publish apps on Google Play. 
    
-   [Get started with custom app publishingOpens in a new tab](https://developers.google.com/android/work/play/custom-app-api/get-started) - Google’s guide to publishing custom apps.
> 