# orion360-sdk-basic-hello-ios
Repository for Orion360 SDK Basic for iOS, Hello

# Examples for Orion360 SDK (Basic) for iOS
![3fda62e0-79e6-11e6-9f00-15bb10c29dd3](https://user-images.githubusercontent.com/36510685/36898354-379b03e0-1e23-11e8-8876-50a71b2043f5.png)

This repository contains a simple 360° image viewer iOS application written in Swift.

Features:

-   Play one hard coded image (from URL)
    
-   Sensor fusion (acc+mag+gyro+touch)
    
-   Panning (gyro, swipe)
    
-   Zooming (pinch)
    
-   Full screen view locked to landscape
    

The Orion360™ SDK Basic can be used for iOS projects using Swift and/or Objective-C.

Before using the SDK, read the [Licence Agreement](https://github.com/FinweLtd/OrionSDK_iOS_Prd/blob/master/Finwe_Orion360_SDK_Basic_Evaluation_Kit_License_en_US-20161212_1500.pdf).

Table of Contents
-----------------
1. [Introduction](#introduction)
2. [Overview](#overview)
3. [Prerequisites](#prerequisites)
4. [Supported Devices](#supported-devices)
5. [Installation](#installation)
6. [CocoaPods installation guide](#cocoapods-installation-guide)
7. [Getting started with Xcode and creating new project](#getting-started-with-xcode-and-creating-new-project)
8. [Getting started with Podfile](#getting-started-with-podfile)
9. [Create Podfile](#create-podfile)
10. [Open Podfile in edit mode](#open-podfile-in-edit-mode)
11. [Edit the Podfile](#edit-the-podfile)
12. [Adding Orion360 SDK to our project](#adding-orion360-sdk-to-our-project)
13. [Start new Xcode session](#start-new-xcode-session)
14. [Working on OrionImageViewer xcworkspace](#working-on-orionimageviewer-xcworkspace)
15. [Objective-C bridging header for Swift projects](#objective-c-bridging-header-for-swift-projects)
16. [Obtaining License File](#obtaining-license-file)
17. [Let us start to have fun with coding](#let-us-start-to-have-fun-with-coding)
18. [Run OrionImageViewer](#run-orionimageviewer)
19. [Next Steps](#next-steps)



## Introduction

The Orion360™ SDK Basic for iOS is a developer library to easily build and implement mobile applications that utilize immersive 360° video and 360° image content.

360° video/image is a special type of content that covers the complete surroundings of the camera. Using our SDK, 360° content can be included into mobile apps easily.



## Overview

The Orion360 SDK Basic for iOS provides a new iOS library that can be included to 3rd party iOS apps and that greatly simplifies building an app that supports 360° video/image content.

Using our SDK showing a single 360° video/image from the remote URL or from local file system requires only a few lines of code. This is achieved by providing a 360° video/image player component which enables the player to be simply dropped into a UI layout and initialized with a handler to 360° video/image.

In short, Orion360 contains one main component “Orion1View” and its purpose is to view and play 360-degree content. 

## Prerequisites

The Orion360 SDK for iOS requires the standard development environment for iOS apps (Xcode Developer Tool).

## Supported Devices

Orion360 for iOS supports all iOS devices starting iOS version 7.0.

## Installation

The easiest way to take the SDK to use is to utilize the CocoaPods framework.

What is CocoaPods?

CocoaPods is the dependency manager which takes care of frameworks and third-party dependencies for your Xcode Projects. To use Orion360 SDK in your project, you need to install CocoaPods. Please follow installation guide below.

Note: If CocoaPods is already installed on your Mac you can skip this.

To check if CocoaPods is already installed or not, Open terminal and type the following command and press Return key (↵).

	pod install ↵

If CocoaPods is not installed, the following error log will be shown on terminal

	-bash: pod: command not found

### CocoaPods installation guide:

On terminal type, the following command and press Return key.

	sudo gem install cocoapods ↵

Note: Your machine might ask for your system password, type your password and press Return key. (Tip: you will not be able to see what you are typing while entering your password, make sure you press Return key after you finish entering your password). If the correct password is given CocoaPods will start the process of installation.

You can read more about CocoaPods and installation guide on: [http://guides.cocoapods.org/using/getting-started.html#installation](http://guides.cocoapods.org/using/getting-started.html#installation)
## Getting started with Xcode and creating new project

<img width="87" alt="screen shot 2018-02-27 at 13 14 21" src="https://user-images.githubusercontent.com/36510685/36898414-71b5ced4-1e23-11e8-9749-f60cdb107549.png">

Figure 1. Xcode Developer Tool

Open Xcode from the /Applications directory.

If this is the first time you’ve launched Xcode, it may ask you to agree to the user agreement and to download additional components. Follow the prompts through these screens until Xcode is completely set up and ready to launch.

As soon as Xcode launches, the welcome window appears (See Figure 2).

<img width="450" alt="screen shot 2018-02-27 at 13 17 38" src="https://user-images.githubusercontent.com/36510685/36898486-bac2233e-1e23-11e8-8095-c2e3f15fa45d.png">

Figure 2. Xcode’s Welcome window

From the welcome window, click “Create a new Xcode project” (or choose File > New > Project). Xcode opens a new window (Figure 3) and displays a dialog in which you choose a template.

<img width="715" alt="screen shot 2018-02-27 at 13 30 56" src="https://user-images.githubusercontent.com/36510685/36898520-d8e241aa-1e23-11e8-9658-fbb966506b4e.png">

Figure 3. Xcode’s window for choosing template

Select iOS from top of the dialog box and choose Single View App from Application section and then click Next to choose options for your project (Figure 4).

![screen shot 2018-02-27 at 13 35 21](https://user-images.githubusercontent.com/36510685/36898549-044c5128-1e24-11e8-9360-cb3b17c36dc8.png)

Figure 4. Additional options for your project

In the dialog that appears (Figure 4), use the following values to name your app and choose additional options for your project:

-   Product Name:  OrionImageViewer
    
-   Xcode uses the product name you entered to name your project and the app.
    
-   Team:  If this is not automatically filled in, set the team to None.
    
-   Organization Name:  The name of your organization or your own name. You can leave this blank.
    
-   Organization Identifier:  Your organization identifier, if you have one.
    
-   Bundle Identifier:  This value is automatically generated based on your product name and organization identifier.
    
-   Language:  Swift or Objective-C, depending on your preference. For this example, we are using Swift
    
-   Devices: Universal
    
-   A Universal app is one that runs on both iPhone and iPad.
    
-   Use Core Data: Unselected.
    
-   Include Unit Tests: Unselected.
    
-   Include UI Tests: Unselected.
    

Click Next. In the dialog that appears, select a location to save your project and click Create.

Xcode opens your new project in the workspace window (See Figure 5).

![screen shot 2018-02-27 at 13 45 01](https://user-images.githubusercontent.com/36510685/36898619-4d6bfdfe-1e24-11e8-8819-32227961a1e5.png)

Figure 5. OrionImageViewer’s project workspace

As seen in Figure 5, CocoaPods is not yet added to our project. Step 2 of this documentation will guide you through CocoaPods and SDK installation.

## Getting started with Podfile

Go to terminal and navigate to project directory (OrionImageViewer). You can navigate using two ways. Either by navigating to project directory using cd \[type directory name\] or simply type cd and drag & drop your project directory on terminal and terminal will insert directory path for you, then press Return key.

	cd <drag and drop your project folder> ↵

## Create Podfile

Type pod init and press Return key to create empty pod file for your project directory. Podfile is what you use to specify all the required libraries for your project.

	pod init ↵

After running pod init Podfile is added to your project directory.

![screen shot 2018-03-01 at 10 29 37](https://user-images.githubusercontent.com/36510685/36898656-6d34b086-1e24-11e8-9b5a-e1934be8c48e.png)

Figure 6. OrionImageViewer’s directory after pod init

## Open Podfile in edit mode

Type the following command on the terminal to open Podfile in edit mode.

	open -e Podfile ↵

After opening the Podfile, you Podfile contents will look like Figure 7

![screen shot 2018-02-21 at 11 00 17](https://user-images.githubusercontent.com/36510685/36898838-311de012-1e25-11e8-8292-5c92e198068e.png)


Figure 7. Podfile content before being edited

## Edit the Podfile

Edit the Podfile content as follows to Install Orion360 SDK Basic for iOS:

	source 'https://github.com/FinweLtd/PodSpecs_Prd.git'  
	source 'https://github.com/CocoaPods/Specs.git'  
	  
	target 'OrionImageViewer' do  
	\# Comment the next line if you're not using Swift and don't want to use dynamic frameworks  
	use_frameworks!  
	  
	\# Pods for OrionImageViewer  
	pod 'OrionSDK'  
	end

## Adding Orion360 SDK to our project

After saving the updates you made on Podfile, go to terminal and type the following command and press Return key (↵)

	pod install ↵

After few minutes you will see a log something like Figure 8 on your terminal.

![screen shot 2018-02-28 at 9 35 09](https://user-images.githubusercontent.com/36510685/36898894-6db44732-1e25-11e8-8176-8d162a25b470.png)

Figure 8. Orion360 SDK installation completed

If you see message “Pod installation complete!”, you are ready to add our Orion360 SDK to your project and start to have fun :)

Open project directory and you will see OrionImageViewer.xcworkspace added (see Figure 9)

![screen shot 2018-02-21 at 11 21 07](https://user-images.githubusercontent.com/36510685/36898935-9af0bab4-1e25-11e8-8ebf-346cec8f4142.png)

Figure 9. Project directory’s content after successful pod installation.

## Start new Xcode session

After successful pod installation, on the terminal you will see:

\[!\] Please close any current Xcode sessions and use \`OrionImageViewer.xcworkspace\` for this project from now on.

Close opened Xcode project and open `OrionImageViewer.xcworkspace`. From here on you should work on `OrionImageViewer.xcworkspace’.

![screen shot 2018-02-21 at 11 27 01](https://user-images.githubusercontent.com/36510685/36898955-af46f8e8-1e25-11e8-9392-c7c05cdc4154.png)

Figure 10. OrionImageViewer.xcworkspace.

Notice: Whenever there will be a new update to the Orion360 SDK, go back to Step 2 and write pod update command and press Return key, and SDK will be updated right away.

	pod update ↵

## Working on OrionImageViewer xcworkspace

After opening OrionImageViewer.xcworkspace you can see the SDK is successfully added to our project (see Figure 11).

![screen shot 2018-02-21 at 11 54 23](https://user-images.githubusercontent.com/36510685/36898976-c7d194fe-1e25-11e8-9a1d-6e29d2f78a63.png)

Figure 11. OrionImageViewer’s project structure after pod install

  ![seq1](https://user-images.githubusercontent.com/36510685/36898999-e12501ac-1e25-11e8-93f4-5ce6eb3b9636.png)

Figure 12. Sequence diagram:Orion1View

The Orion360 SDK can be used for both Objective-C and swift project. For Objective-C project you simply import Orion1View (#import <Orion1View.h>) header and initialize it as follows:

	Orion1View orion1View = \[\[Orion1View alloc\] initWithFrame:CGRectMake(0, 0, self.view.bounds.size.width, self.view.bounds.size.height)\];  
	orion1View.delegate = self;

  

Note that the license file need to be given.

	NSString\* path = \[\[NSBundle mainBundle\] pathForResource:@"license.key.lic" ofType:nil\];  
	NSURL *licenseURL = \[NSURL fileURLWithPath:path\];

  

For Swift projects you need to create bridging header. Please follow Step 9. (For Objective-C projects, skip Step 9 and jump to Step 10 to learn how you can acquire Orion360 SDK)

  

## Objective-C bridging header for Swift projects

Create bridging header as follows:

File > New > File > (iOS, watchOS, tvOS, or macOS) > Source > Objective-C File

![screen shot 2018-02-21 at 12 18 24](https://user-images.githubusercontent.com/36510685/36899032-050eb91e-1e26-11e8-849f-54807ce8b3f0.png)

Figure 13. Create new Objective-C file for bridging header

![screen shot 2018-02-23 at 13 13 48](https://user-images.githubusercontent.com/36510685/36899090-391f8b0c-1e26-11e8-95a2-a10135d66e5f.png)

Figure 14. Create new Objective-C file for bridging header

Give file name which is similar to your project name for this example "OrionImageView" and press Next, and save it in the same directory as your project.

If you accept, Xcode creates the header file along with the file you were creating, and names it by your product module name followed by "-Bridging-Header.h". When you press Create you will see a dialog message (see Figure 15) and click on “Create Bridging Header”

![screen shot 2018-02-21 at 12 23 12](https://user-images.githubusercontent.com/36510685/36899104-4bad682a-1e26-11e8-8d27-07f0701290bd.png)

Figure 15. Creating bridging header

![screen shot 2018-02-28 at 10 07 02](https://user-images.githubusercontent.com/36510685/36899150-7cb02282-1e26-11e8-8355-c9a2b5b9f4f1.png)

Figure 16. OrionImageViewer’s project structure after creating bridging header

Now open OrionImageViewer-Bridging-Header.h and type #import "Orion1View.h" and save the file.

![screen shot 2018-02-21 at 12 32 33](https://user-images.githubusercontent.com/36510685/36899173-99ca917c-1e26-11e8-91ca-a3691b5a2373.png)

Figure 17. Importing Orion360 SDK using import statement

 After creating bridging header find the  class line, which should look like this:
	 class  ViewController: UIViewController {
    
After UIViewController, add a comma (,) and  Orion1ViewDelegate and initialize Orion1View as follows:

	let orionView = Orion1View(frame: CGRect(x: 0, y: 0, width: view.bounds.size.width, height: view.bounds.size.height))  
	orionView.delegate = self

And license file is given as follows:

	let path: String? = Bundle.main.path(forResource:"Orion360\_SDK\_Basic\_iOS\_Trial_finwe.OrionSimpleVideoPlayer.lic", ofType: nil)  
  	let licenseUrl = URL(fileURLWithPath: path ?? "")

## Obtaining License File

To show 360° content you need a license file that must be added to your app project's resources without any modification. Failure to do so will result to black video player screen and currently, it doesn't produce any warning messages.

Orion360 SDK is a commercial product and requires a license file to work. An evaluation license is provided with the sample app. You can get a watermarked evaluation license file also for your own bundle identifier by creating an account to [https://store.make360app.com](https://store.make360app.com/), starting a new SDK project, providing your own package name, and selecting FREE Trial.

Please follow these steps to obtain License File:
1.  Go to  [https://store.make360app.com](https://store.make360app.com/)
    
2.  Sign in if you have an existing account with us or Sign up if you are a new user.
    
3.  After successful login click on New SKD Project button
    

![screen shot 2018-02-21 at 12 45 40](https://user-images.githubusercontent.com/36510685/36899227-de93e2ea-1e26-11e8-9287-8e64bf32d8fa.png)


4.  Give Project Name, and Package Identifier as they are written on Identity section
    

![screen shot 2018-02-21 at 13 12 27](https://user-images.githubusercontent.com/36510685/36899299-1a912ef6-1e27-11e8-951b-deb8e4d127be.png)

Figure 18. Select your project from target

Click on your project from Project Navigator > Select your target > choose General > Identify


![screen shot 2018-02-21 at 12 56 56](https://user-images.githubusercontent.com/36510685/36899265-fc3109d6-1e26-11e8-84e7-2b7c0ff25add.png)

Figure 19. Bundle Identifier = Package Identifier, Display Name = Project Name

5.  Select iOS on Platforms section
    
![screen shot 2018-02-21 at 13 17 31](https://user-images.githubusercontent.com/36510685/36899320-32454bcc-1e27-11e8-819f-1e721777f884.png)

Figure 20. Target platforms

6.  Choose type of license, payment method
    
![screen shot 2018-02-21 at 13 18 33](https://user-images.githubusercontent.com/36510685/36899341-4938f1d0-1e27-11e8-9e68-ad08025de0c0.png)

Figure 21. Payment method

And click on Free Trial or Purchase

7.  Read and agree to our terms and regulations
    

Click on Accept after reading Orion360 SDK Basic Evaluation End-User License Agreement (EULA)

![](https://lh5.googleusercontent.com/v_zsq3y1-d0Oj1G4ATgeWeW5BXiih1hj10c-2Q-NFPlnydFJ5Hs9veFfgmPXv2zyC8tqq4CKQ0E9ErnHNBaZXt_Xu6leydSWSDs14rzN3_EwbssPwG3C2mLW64-PhNPlp2O5R0Zz)

Figure 22. Orion360 SDK’s EULA

Once again click Accept to Terms & Conditions

![screen shot 2018-02-21 at 13 21 59](https://user-images.githubusercontent.com/36510685/36899356-64a7e502-1e27-11e8-81e1-e876d8b1e129.png)

Figure 23. Orion360 SDK’s Terms & Conditions

After accepting both terms, you will get a notification which says “Your new licenses are ready to be downloaded. Scroll down to the Downloads section to get them.”

![screen shot 2018-02-21 at 13 24 11](https://user-images.githubusercontent.com/36510685/36899430-c97be4ec-1e27-11e8-85fb-02fbbb6054e7.png)

Figure 24. Downloads for extracted license

Click on “Download iOS Basic Trial Licenses”.

8.  Add the downloaded license to your project
    

Extract the download file.  
Select “Orion360\_SDK\_Basic\_iOS\_Trial_finwe.OrionImageViewer.lic“, drag the file and drop it inside Project navigator under your project folder and click Finish.

![screen shot 2018-02-21 at 13 33 21](https://user-images.githubusercontent.com/36510685/36899536-3477eb10-1e28-11e8-82a2-52b825a62f56.png)

Figure 25. Adding license file (.lic) to project directory

![screen shot 2018-02-28 at 13 13 12](https://user-images.githubusercontent.com/36510685/36899577-60e5d112-1e28-11e8-858a-b7188b3dfc18.png)

Figure 26. Project structure after license file added

  

## Let us start to have fun with coding
Swift

	ViewController.swift

	//
	//  ViewController.swift
	//  OrionImageViewer

	//  Copyright (c) 2018 Finwe Ltd. All rights reserved.
	//

	/**
	 * This is an example of Orion1Image viewer.
	 *
	 * Features:
	 * - Plays one hardcoded 360x180 equirectangular image
	 * - Image can be from URL or local repository
	 * - Sensor fusion (acc+mag+gyro+touch)
	 * - Panning (gyro, swipe)
	 * - Zooming (pinch)
	 * - Fullscreen view locked to landscape
	 */

	import UIKit

	class ViewController: UIViewController, Orion1ViewDelegate
	{
	    
	    override func viewDidLoad()
	    {
	        super.viewDidLoad()
	        
	        //Create an instance of Orion1View and initialize it as follows
	        let orionView = Orion1View(frame: CGRect(x: 0, y: 0, width: view.bounds.size.width, height: view.bounds.size.height))
	        orionView.delegate = self
	view.addSubview(orionView)
	        //Add license URL
	        let path: String? = Bundle.main.path(forResource: "Orion360_SDK_Basic_iOS_Trial_finwe.OrionImageViewer.lic", ofType: nil)
	        let licenseUrl = URL(fileURLWithPath: path ?? "")
	        
	        // Image can be given from URL or local repository
	        
	        //Image URL
	        let photoUrl = URL(string: "https://s3.amazonaws.com/orion360-us/Orion360_example_image_1_4096x2048.jpg")
	        

	        
	        // Set Image and license url and you are done!!!
	        orionView.initImage(with: photoUrl, licenseFileUrl: licenseUrl)
	        
	    }
	    
	}

Note: If you are using images/video from URL, make sure your sources are from HTTPS. Apple’s ATS Policy,  App Transport Security start blocking a cleartext HTTP (http://) resource load since it is insecure. Temporary exceptions can be configured via your app's Info.plist file.
The above example displays image from URL, if you want to show an image from a local repository, add your image to Assets and initialize the photoUrl variable as follows: 

Note:  If you are using images/video from URL, make sure your sources are from HTTPS. Apple’s ATS Policy, App Transport Security start blocking a cleartext HTTP (http://) resource load since it is insecure. Temporary exceptions can be configured via your app's Info.plist file.

The above example displays image from URL, if you want to show an image from a local repository, add your image to Assets and initialize the photoUrl variable as follows:

	//Photo from local repository  
	let photoUrl = UIImage(named: "YourImageName.jpg")

  

## Run OrionImageViewer

The Scheme pop-up menu lets you choose which simulator or device you’d like to run your app on. As seen on Figure 27 iPhone 8 Plus Simulator, not an iOS device.

 ![screen shot 2018-02-27 at 14 41 14](https://user-images.githubusercontent.com/36510685/36899595-7d711f30-1e28-11e8-9a08-4d3779031255.png)

Figure 27. Xcode’s toolbar

Save the changes and click the Run button <img width="20" alt="screen shot 2018-02-27 at 14 45 45" src="https://user-images.githubusercontent.com/36510685/36899661-c9c139ba-1e28-11e8-88bc-fe104efb3747.png"> or press ![screen shot 2018-02-27 at 16 23 48](https://user-images.githubusercontent.com/36510685/36899715-07afe5aa-1e29-11e8-9a03-17ecb10b8797.png) to build and run OrionImageViewer and you are able to see a beautiful picture from Lapland Finland. Feel free to play around with the image by zooming, panning and rotating. Explore Finnish winter and beautiful landscape in one picture :)

![screen shot 2018-02-27 at 14 51 34](https://user-images.githubusercontent.com/36510685/36899622-a0909612-1e28-11e8-85b2-3061da9df135.png)

![screen shot 2018-02-27 at 15 07 31](https://user-images.githubusercontent.com/36510685/36899631-adcd124c-1e28-11e8-862b-2de929a32231.png)

![screen shot 2018-02-27 at 15 31 10](https://user-images.githubusercontent.com/36510685/36899636-b173aba4-1e28-11e8-9a79-6296aab25424.png)

Completed version of OrionImageViewer can be downloaded [here](https://github.com/FinweLtd/orion360-sdk-basic-hello-ios.git).

## Next Steps


It is recommended to get familiar with the [wiki](https://github.com/FinweLtd/OrionSDK_iOS_Prd/wiki) pages and API documentation that is included in the SDK to learn more about the available features and how they should be used.

To jump start your project, take a look at the delivered sample apps: Objective-C: [https://github.com/FinweLtd/Orion\_SDK\_iOS_SampleApps](https://github.com/FinweLtd/Orion_SDK_iOS_SampleApps) , Swift: https://github.com/FinweLtd/orion360-sdk-basic-examples-ios

Import the project to your workspace, build and run it on your device. Then look at the source code.

## Feedback & Support


Feedback & support should be directed via email to support@finwe.fi
