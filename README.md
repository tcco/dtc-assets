# Overview

Handing off password protected assets to developers!

## Backend

```text
The ams-backend.zip contains a boilerplate template using our internal up-py-common 
(copied in by hand) as well as FastAPI as a web framework. Please download and follow 
the README.md in order to get started. Once you run make run go to endpoint 
http://localhost:5000/docs to see the auto generated Swagger and how they’re auto-generated 
from the code. The one internal tool you should drill into is in up_py_common.pynamodb_utils 
which helps utilize DynamoDB in these given tools.

Getting acquainted with the tools in the setuptools file as well as thinking through what 
would be useful in future would be a great start. To give a teaser, we’re obviously looking 
to put together a service that manages affiliate networks at a shop level initially, but 
search capability, categorization, internal portal management, and eventually maintaining 
a product level relationships. But more to come there in future discussions.
```

## iOS

```text
Following up on a separate thread for the codebases / technical guidance. Attached are the 
SDK as it stands and the initial app we used the SDK with, BookAnywhere. We'll aim to have
a knowledge transfer with the original maintainers later this or early next week.

There are two parallel tracks we'll be pursuing: updating our SDK to our latest internal 
version v5 and building a mobile app that integrates WebView overlays with our latest SDK. 
These code bases are 2 years old so it'll be good to understand what needs to be modernized. 
The SDK will need to maintain backwards compatibility but the mobile app only needs to be 
compatible for latest versions to reduce complexity.

SDK

- Personally I was unable to get this repository to build. We can follow up more in our knowledge transfer conversation here in near future
- I manipulated UpliftSDK/ProductionScripts/SDKCopy.sh to use the current directory as the ROOT_FOLDER which was a step in the right direction but still failed at a following step
- Sample apps are provided in Quest3 and SampleApp directories
- In regards to upgrading our SDK, please begin to understand ULApi.m where the offer and order methods will be sunsetted

BookAnywhere

- pod install as well as carthage update from BookAnywhere directory. However you likely won't need to do this given I've zipped everything up
- I had to comment out all references to UPIdentity because I was unable to download properly from internal repositories. Feel free to comment out as necessary to get the build to work
- This app should serve as a point of reference rather than the actual code base we're going to work on! 
```

## Android

Todo
