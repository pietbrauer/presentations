# __Modular__ iOS Apps

---

# __GOALS__

---

## __divide__ the XING iOS App into logical parts

---

## __make it easier__ for new coworkers to get started

---

## enable __versioning__ in the different modules

---

## __slim down__ the main app

---


## make other product teams __more productive__

---

## write __cleaner code__ due to segmentation

---

# __HOW__

---

* CocoaPods
* Rake
* Jenkins
* Ruby command line tool

---

### each module has a podspec

---

### private cocoapods specs repository on GitHub Enterprise

---

### Jenkins builds the spec repo on every pull request and checks for valid podspecs 
### __Just like the real Specs Repo__

---

## __unified rake tasks__ for each project

----

    rake build
    # builds the project for CI

    rake version:bump:minor
    # bumps minor, patch and major version number


    rake git:release
    # tags the version and pushes to master
    
    rake pod:push
    # pushes the podspec to the master repo

---

## Ruby CLI

* based on Thor gem
* heavily uses Xcodeproj from Cocoapods

---

    $ xcnew help new
    
      Usage:
  	  xcnew new PROJECTNAME PREFIX

	  Description:
  	  `xcnew new` creates a new XING iPhone App module project 
  	  to get you up and running in no time.

  	  It will create our desired file structure for modules,
  	  install our dependencies and create simple Xcode project 
  	  with Login using the XNGAPIClient.
    
    $ xcnew new XNGCocoaHeads CH

---

# *DEMO*

---

# __MODULES__

---

### __13__ core modules extracted
### __21__ other modules (regular pods)

---

## XNGUIKit


### UIDevice, UIImage, UIImageView, ... categories and subclasses

---

## XNGFoundation

### NSString, NSArray, NSDictionary, ... categories and subclasses

---

## XNGDataModel

### CoreData model, mogenerator models, models, datafetcher etc.

---

## BaseViewControllers

### UIViewController, UICollectionVC, UITableVC, ...

---

## Other Modules
### Login, Walkthrough, Register, XNGFont, XNGColor, Tracker ...

---

# What's __next__?

---

## port the installer to cocoapods

GitHub: pietbrauer/cocoapods-generate-command

---

### Apply modules pattern to network news, profile etc. once the small issues are resolved

---

## Find more iOS developers.

---

## Build more modules.

---

## Answer your questions.

---

## Thanks !

### @piet_nbn
