# orion360-sdk-basic-hello-ios
Repository for Orion360 SDK Basic for iOS, Hello

# Examples for Orion360 SDK (Basic) for iOS
**![](https://lh5.googleusercontent.com/M5eWUi908Ce5JW7jkXUdduMN44riSl-2dscMggx_o48AQ62h_2nYea22NAlcl82PcJeQ_q3GHJR0iSjr8Vvi_0j13vxvSK0Pr33qfKwogmN9muWZR2efC6wBLr9COaUUoxmMGIrp)**

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

![](https://lh5.googleusercontent.com/tYMGkEVzmRRwHjXilPdEepW283bX_ViaEAkPZNIrpcRntMst5RCKTpom9v0wVneYqeJeBBotUudEbMZAI3ux11V612r9wr01BHWDtv7IOntPe-gOqryg5KAwmCiWM3zSdkKEoFTj)

Figure 1. Xcode Developer Tool

Open Xcode from the /Applications directory.

If this is the first time you’ve launched Xcode, it may ask you to agree to the user agreement and to download additional components. Follow the prompts through these screens until Xcode is completely set up and ready to launch.

As soon as Xcode launches, the welcome window appears (See Figure 2).

![](https://lh5.googleusercontent.com/ZFZ4U3lFDOcUA8BWDQCujZx8eX0XCsfxRPIF3kko7jhrcL4c9qy8aX9Uo_TAl2J7JKFDOfwQnC_0si5GdTPzBic6fAgMezzsNCWn-QYTQA95VQhzSouhd5ngfvRFq_p1tdb--uOr)

Figure 2. Xcode’s Welcome window

From the welcome window, click “Create a new Xcode project” (or choose File > New > Project). Xcode opens a new window (Figure 3) and displays a dialog in which you choose a template.

![](https://lh5.googleusercontent.com/TOrIvzJDGs8qOUg_bhPsqCliUexAUqDrU0x3aTB7UKgj5F-DzWHvQ4GoyDDh077-mhG5cT9OZ2YA80umlniPcjx06OG3mZlRIequzcfOmg2qc4mWl2T9XZry92P_rbTN7_JOeSgB)

Figure 3. Xcode’s window for choosing template

Select iOS from top of the dialog box and choose Single View App from Application section and then click Next to choose options for your project (Figure 4).

![](https://lh5.googleusercontent.com/GC0fYEtTh3vFGPWzmf8TS5s_KEbGja2GSD_hsZPFcd04lfJWydK012x7pUfiwyDfxw4O69UtQFaHOtZATtIpwy6vVDwCh24vbGzHszE8W_IjaZ74VlSdebIBgN2TPohh5KRSyIwT)

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

-   ![](https://lh4.googleusercontent.com/fcNXCDV4eI5DnIJqFa05gMvwy1UaCWX1jpzo_Ta1OSD7gscmRL0fzvx6OtG-PEjQFOVuszarSDVaO3yjHmCbmYHDISzVfGcG--V-YXpvb77CjT06iOX4ZGjGoUnsfVai8oalyr3M)
    
-     
    

Figure 5. OrionImageViewer’s project workspace

As seen in Figure 5, CocoaPods is not yet added to our project. Step 2 of this documentation will guide you through CocoaPods and SDK installation.

## Getting started with Podfile

Go to terminal and navigate to project directory (OrionImageViewer). You can navigate using two ways. Either by navigating to project directory using cd \[type directory name\] or simply type cd and drag & drop your project directory on terminal and terminal will insert directory path for you, then press Return key.

	cd <drag and drop your project folder> ↵

## Create Podfile

Type pod init and press Return key to create empty pod file for your project directory. Podfile is what you use to specify all the required libraries for your project.

	pod init ↵

After running pod init Podfile is added to your project directory.

![](https://lh6.googleusercontent.com/qoHpIQ3p-3SPyCD-gnjsdj7OnEEzC8D0LlUdWTgycavalj6bkZvBzmjEXlQxUB3FTCmLJP77VRHCDGWKrGRQfkS4gRl0sy-FmVPRdm2kKLdq9UvfeTJB35xMgG4vie91SrRmX9gI)

Figure 6. OrionImageViewer’s directory after pod init

## Open Podfile in edit mode

Type the following command on the terminal to open Podfile in edit mode.

	open -e Podfile ↵

After opening the Podfile, you Podfile contents will look like Figure 7

![](https://lh5.googleusercontent.com/N69deL_RUoXdwC32CA-LRquZ6y-FiC2IDSfN5l83I5M7Gi8rdK8Y5RMUmD4lMc2whS4BAjLM463Txw_puOIbzvtjRieZ_6g4CVbwAXwtC-GTTL_PD76VVB2cFfQnDnnB3C832yT0)

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

![](https://lh3.googleusercontent.com/CCo9K1PYVYOLGJpaxqh_vC_9xQ6nMQPoM-bW-w7fvWsZb8958I5O8uxGPLkthZKGRrKe1LHRDKuPC3cj2JIxkIn9hBGagHwHHqjKonDMivFQ9JcDOXCeDz_lJzJKRJn-ITnhjAFt)

Figure 8. Orion360 SDK installation completed

If you see message “Pod installation complete!”, you are ready to add our Orion360 SDK to your project and start to have fun :)

Open project directory and you will see OrionImageViewer.xcworkspace added (see Figure 9)

![](https://lh4.googleusercontent.com/aM6eeN_a5fLxScgz2YhXz7UAY51Uh9XYsoIrIXM5BnYW2xwysuckqoBq_F1VSlD6GIg9VPSlIkAw6Yzw0TQURC5hYbq9F7bp0Dc3H1RlSeXVU8XWeQoPqalvSIdh01FjfPQ925WP)

Figure 9. Project directory’s content after successful pod installation.

## Start new Xcode session

After successful pod installation, on the terminal you will see:

\[!\] Please close any current Xcode sessions and use \`OrionImageViewer.xcworkspace\` for this project from now on.

Close opened Xcode project and open `OrionImageViewer.xcworkspace`. From here on you should work on `OrionImageViewer.xcworkspace’.

![](https://lh6.googleusercontent.com/oBEZcDVaAwHDXCC9ZEzsSQs_MfFpkVBNFeDl4pKmn3sPrMhe97MZdkM9LtK9M85V_PDGAbbZNmDdv87aljsqTk52hULc1nVmwWVXxp-K7tBKVpO4Q7p-QsoscQJ_K2iAHxyFCvTW)

Figure 10. OrionImageViewer.xcworkspace.

Notice: Whenever there will be a new update to the Orion360 SDK, go back to Step 2 and write pod update command and press Return key, and SDK will be updated right away.

	pod update ↵

## Working on OrionImageViewer xcworkspace

After opening OrionImageViewer.xcworkspace you can see the SDK is successfully added to our project (see Figure 11).

![](https://lh4.googleusercontent.com/Ik53YeAXdfNabB2ZFKSGoG1N1e9ua2K4GJpeyIAcqNUaGImUigTxIDUP9YpCwqLqF523ebVqsDotsvPaDmyUmr7FSsy2PF_oxlr9gXhoKyfMq2Y-8YesLD-PzS_l8Zh56o6g0kT9)

Figure 11. OrionImageViewer’s project structure after pod install

  

![](https://lh4.googleusercontent.com/305sLNiPcnAmQcI4q5GTWfJ3IGKSyRAFR8hj3D-jEe36Ps2zd_EHRHEKhexBs9cFb2XWcuVyVY6rgeggqVWagw5imhbpkiM_bs0Qzaehn9F7Z0BEaqiXEt3Z-desLRv6idRbuuS1)

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

![](https://lh6.googleusercontent.com/GkGZSX-QKBn5kDJSWIgVw6V5uLcFscWjO3KKn173Xbhx28v5ljfJlLyyCCWO4xAGFNCKA0QfmlBUug2pYBRqx65DSoKtOVQ55LcEIM4kBrTKEZQRv8-T2fivvk7y0MndtaMddxwG)

Figure 13. Create new Objective-C file for bridging header

![](https://lh5.googleusercontent.com/8VzHTNrS-cHVcAOMuY-fPOB0G78z2jpewXWF-j9v_zGoLYmmLVy9fy1dXfGX4kneobYElsxhfkaBv-PyPiWMGOfoBCVOm1sVMnhKLl57GYj3Qdqm6v09us2jHMgrE0gVgLfDibiy)

Figure 14. Create new Objective-C file for bridging header

Give file name which is similar to your project name for this example "OrionImageView" and press Next, and save it in the same directory as your project.

If you accept, Xcode creates the header file along with the file you were creating, and names it by your product module name followed by "-Bridging-Header.h". When you press Create you will see a dialog message (see Figure 15) and click on “Create Bridging Header”

![](https://lh5.googleusercontent.com/vYFF5AFYNpw5bMUy5Skfo1pt3VBOQiXmjzejPdDPq8ene5JY0OcOIF8Rv6W7Qnszi3oppQHxQAyxCnP4Yp6g7lakWHtfYanJBXzO9j70rtGsj0EcxM68vpmV5XOAWNn6n6x-iJ7b)

Figure 15. Creating bridging header

![](https://lh6.googleusercontent.com/eInhcrgDErw8I7CJNQQelABs5RblPp7ra7Oh0GxFi4ULI3OYkJmDMS7B26JkveX7-80EBioWJHemFyURrZLuGaPoHREZV7oyiSQ8lUOpasqN9I4H7YNTWEVZAK_z5MEFm-_x04Rk)

Figure 16. OrionImageViewer’s project structure after creating bridging header

Now open OrionImageViewer-Bridging-Header.h and type #import "Orion1View.h" and save the file.

![](https://lh6.googleusercontent.com/HXxZbwYi1Vx93uQ2U4MMChdjk4DKEKpouOLyfWm7i3Zm3mo_kZMqou157v9pa5iEnCfcu7qszIvhDrB4D71lMCAD0-y6nbl54U9VrjLCAPz3jBvVEQ9BgZBKTex3AvlHq8TfmIPr)

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
    

![](https://lh5.googleusercontent.com/bd15zYZ0jVA1vTdgc9QosFH2FAHcxSUvNZyIv_lopmYwngAzwmhGo-0HZb6fAaDdqH4L80qCL6YCib0NcIUdU99QjgoztVfFGwMlmnw9Ug0e6YJGxNvyh8uXv4sCPbVtRd9dJHDt)

4.  Give Project Name, and Package Identifier as they are written on Identity section
    

![](https://lh4.googleusercontent.com/N9E10Vz9-AzeRWrZ5DNIQZhks-CAitHWZX57va_brimh7hr_CMpKGa7TNLSsxT8_v2Df0O2Q0PXthFcqj44qI4eAchtDZMxYxy2xSeBLDAaFay9PoAjc33KrsPEN9ViULFWUv1We)

Figure 18. Select your project from target

Click on your project from Project Navigator > Select your target > choose General > Identify

  

![](https://lh4.googleusercontent.com/5UhzN21CLT-z5q--pyPXMsp7inADBUCVBCDDZwv9aSN-bzjMDDoQlUv5l2lQNb-8O2jLSOg0eNDMGKMC32DE4yp5mZtdJ8dA1vjCJcUEBEQl3DMBAJZwKmAvWkJ4rRK3eTS8pKCV)

Figure 19. Bundle Identifier = Package Identifier, Display Name = Project Name

5.  Select iOS on Platforms section
    

![](https://lh3.googleusercontent.com/uA7_zHBD_46aft5g3iwNQ8rixoFJUcx1OouIzSpFIgTvJD6F3K1yltzca0T47duP8MCueaTsbO7E2h4As_DkZO_TXda9G_CDHaTU2TcoS4GGSEgK5-6UBr5seaMoJtHqrMtRs3Zy)

Figure 20. Target platforms

6.  Choose type of license, payment method
    

![](https://lh4.googleusercontent.com/wlL78UhweB0mWaH2vZuo0g1yYVIho6R2p3ZOD0Rzvfn5NDqnKIttPglaZivD8QPv0hxvBSDcCUBx687VrB7EyPgmnrwgTt35dvRPe5EtYJ1rFylEhjJqNzffgVYicd3eFNamNRUq)

Figure 21. Payment method

And click on Free Trial or Purchase

7.  Read and agree to our terms and regulations
    

Click on Accept after reading Orion360 SDK Basic Evaluation End-User License Agreement (EULA)

![](https://lh5.googleusercontent.com/v_zsq3y1-d0Oj1G4ATgeWeW5BXiih1hj10c-2Q-NFPlnydFJ5Hs9veFfgmPXv2zyC8tqq4CKQ0E9ErnHNBaZXt_Xu6leydSWSDs14rzN3_EwbssPwG3C2mLW64-PhNPlp2O5R0Zz)

Figure 22. Orion360 SDK’s EULA

Once again click Accept to Terms & Conditions

![](https://lh3.googleusercontent.com/OZTY_vcvIevOkp92xTaLNt68r6QnD0ai4n2OAYKHIZF-wixsYoh5DqLLt8lhbI4ODmvb9Sz_7PEeHePhy44knPCE6YuKQLxpzlJA4CrPEjLgd261R93ujPYhSYOX7h2Je44hAemw)

Figure 23. Orion360 SDK’s Terms & Conditions

After accepting both terms, you will get a notification which says “Your new licenses are ready to be downloaded. Scroll down to the Downloads section to get them.”

![](https://lh6.googleusercontent.com/uPPyC-jcOS5863nEAjse43pqHrDyicqmbPh07XKVrs0RPi1jXHRKeXhPDprANwLGHWN1KYK1CfzgONctzJjk2xNKXJuaWhmDZg-vA9WiSNxGhynik7LZn1t90RlkoaPRa0MGBv4Z)

Figure 24. Downloads for extracted license

Click on “Download iOS Basic Trial Licenses”.

8.  Add the downloaded license to your project
    

Extract the download file.  
Select “Orion360\_SDK\_Basic\_iOS\_Trial_finwe.OrionImageViewer.lic“, drag the file and drop it inside Project navigator under your project folder and click Finish.

![](https://lh4.googleusercontent.com/OW1jMijkLVx7PEdDQ1yFuqnc9xrd5-gEJoaIJrZ0pYWEzVkNKpWf8nKPeXfmL3GoiASkhVWoJs5wkXRsCE6TGB6dKZd9LKB2lnWpzORv7cB2ODWJmshJ3uQOGhdLbuFT4cOs2UaE)

Figure 25. Adding license file (.lic) to project directory

![](https://lh5.googleusercontent.com/AuJ5dIIij08FCDnYeF5qnptomGvPuWw5dbGKIusNYeFxziZXXYN9CB1Ln2Ya5LyVD3CodDuieAs0-OYJsQ0Y5UHdKDeKi6Swx222IxjuZRG-cmH9Ldm8QiYyA3aJuGNsc-Gx_tbH)

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

  

![](https://lh3.googleusercontent.com/kPnDkUjefxvjovwjPMI2Mi1EuLrB0w-08O_j9_cdzG-EnFkcNJfNtjNNIQaLOeehFPlGXG5WvLGBiIFWmTMr6dVVRHUDvAj48nZSRkT5c9YdyGz7kNIeelQ8duc9M2sO7P31tJIU)

Figure 27. Xcode’s toolbar

Save the changes and click the Run button![](https://lh6.googleusercontent.com/hrH1VBPQVqD12srrVpYKvPnJO6cQh_5X_aZ_aAYk9LbAk3mpkKLRdDZ7TX1Pvbxu8spkiH4xWPsJNSwIHirPLlDdCw5FnW6ogkquo15w-r_qaVfqj45w5d33I7EbY1kRMLi1uij4), located in the top-left corner of the Xcode toolbar or press![](https://lh4.googleusercontent.com/Pk_RNpj0ji0hAmWa606P2mYsc-GYJuZTzO7STvee_rZ7ytVtcMN4V5tPkEU1LFGvImvWUj7QAlbu62d5E9TbES2_p_jJ4XaR-GqXnFFPTiMaTknjB504SCCRkadwOPnFMXoNhvN9) to build and run OrionImageViewer and you are able to see a beautiful picture from Lapland Finland. Feel free to play around with the image by zooming, panning and rotating. Explore Finnish winter and beautiful landscape in one picture :)

![](https://lh4.googleusercontent.com/AADaYS81y3uYfldpnB0PS7cn4NogpykmlAuvOGOZQn-i3tIMP-uRQ_hyClfKDtJvEcfTMUoAxkx-sH8oqMLkduB-8GQUd57aPJfB4NCeIx8FgfsI92hZXwDZfek1cqHndP3VWNA0)

![](https://lh4.googleusercontent.com/qvfOF8GK22iEvgAet5OwcL5C2bezx3IE61ISEONdfuBGW8ecA2crC3eX6_3-yGx6Q93efIVVupKQKFNczJrdOyg9Jjh5IxBDq8kbb8pjHancw3fcHTotIOP9N85cZ9ySLXT9ZrJ1)

![](https://lh4.googleusercontent.com/iWvqLTf2PhrmmOoUdsjDC08rd0XVMEuvPnZHCkhO_0Dvf5yj6nWKvVJZZ4BGRcmxRBGjAC-K9sQGaBH0zTveTpCs7svd9Frz-BpIuNKXNSl0V7IPfZeo_tkhpf0q46QdJL25xjJZ)

Completed version of OrionImageViewer can be downloaded [here](https://github.com/teddyFinWe/orion360-sdk-basic-iOS-Swift.git).

## Next Steps


It is recommended to get familiar with the [wiki](https://github.com/FinweLtd/OrionSDK_iOS_Prd/wiki) pages and API documentation that is included in the SDK to learn more about the available features and how they should be used.

To jump start your project, take a look at the delivered sample apps: Objective-C: [https://github.com/FinweLtd/Orion\_SDK\_iOS_SampleApps](https://github.com/FinweLtd/Orion_SDK_iOS_SampleApps) , Swift: https://github.com/FinweLtd/orion360-sdk-basic-examples-ios

Import the project to your workspace, build and run it on your device. Then look at the source code.
