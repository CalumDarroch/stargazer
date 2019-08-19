# StarGazer [![Codacy Badge](https://api.codacy.com/project/badge/Grade/c6e85c7d6c8b416fa266512dba8b4e6e)](https://www.codacy.com/app/StarGeezers/stargazer?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=CalumDarroch/stargazer&amp;utm_campaign=Badge_Grade) [![GitHub contributors](https://img.shields.io/github/contributors/jo-quin/stargazer.svg)](https://github.com/jo-quin/stargazer/graphs/contributors) [![Maintenance](https://img.shields.io/badge/Maintained%3F-no-red.svg)](https://bitbucket.org/lbesson/ansi-colors)

This is our final engineering project for the [Makers Academy](https://makers.tech/) 12 week programing course. We wanted to create an augmented reality phone application that would allow the user to see 3D representations of the stars and planets through their phone camera, placed in their actual locations in the night sky!

Click the image below to see a short video of the app in action:

[![StarGazer demo](https://img.youtube.com/vi/2mJJrip4emc/0.jpg)](https://www.youtube.com/watch?v=2mJJrip4emc)

## Motivation

As a fully self-directed team project, we wanted to take what everything we had learned at Makers about process and engineering principles and apply it to a project that was completely different to anything we had done before. None of us had ever worked on a mobile app, let alone augmented reality software, and we wanted to try and apply the skills we had gained over the past 10 weeks to a completely new challenge, language and tech stack!

This app was chosen from a range of possible projects for a number of reasons:
1. Genuine interest in Augmented Reality - we had wanted to do work with this and experiment with its possible applications for some time, especially after hearing about new AR apps implementing Darknet's [YOLO](https://pjreddie.com/darknet/yolo/).
2. A desire to make something that felt tangible. Previous apps we had designed were web-based, but an AR app would allow the user to interact with their physical environment in a new way, rather than being something that exists purely online.
3. The challenge presented by working with a completely new tech stack, as well as a lower-level language than we had ever used before in Swift. This drove us to learn _a lot_ in a very short space of time to overcome obstacles in the development process.
4. The ambitious nature of the project would mean we would have to stick to best practices and work efficiently as a team. This would be a great test of our skills in agile development, as we would need to have daily stand-ups and implement sprints and good delegation to keep the project on-track.

We organised our task list using GitHub's [Project Card Wall](https://github.com/jo-quin/stargazer/projects/1) feature and kept detailed records of our successes, failures, difficulties and learning in our [GitHub Wiki](https://github.com/jo-quin/stargazer/wiki).

## Installation

To download and install the app, you will need an up-to-date copy of [Xcode IDE](https://apps.apple.com/us/app/xcode/id497799835?mt=12) and an iPhone running iOS 11 or higher. If you are new to Xcode (as we were!) you can find Apple's support documentation [here](https://developer.apple.com/support/xcode/) to help you get started.

Once you have Xcode up-and-running, you can install the app on your iPhone as follows:

1. Clone or download the StarGazer repository.

2. Open the `stargazer` directory in Xcode.

3. Connect your iPhone to your computer via USB (note you will need an apple ID and password to install the app, you can create one [here](https://support.apple.com/en-gb/HT204316)).

4. Run the build using the play button in the Xcode IDE.

NOTE: The first time you try to run the app from your phone you will get a message saying "Untrusted Enterprise Developer" and the app won't launch. To solve this, do the following:
```
-> Settings
-> General
-> Device Management
-> Select the untrusted developer (it will be your apple ID)
-> Click "Trust" to allow you to run the app
```

Now run the app, look around and enjoy the view of the stars and planets from your iPhone! :iphone: Tapping the screen will bring up the names of the celestial bodies, tapping again will remove them.

## Technologies used

* [Xcode IDE](https://developer.apple.com/xcode/ide/) - as well as being a text editor, this handled our CI/CD for the project and ran tests in real-time.

* Language: [Swift](https://swift.org/).

* Apple iOS frameworks:
  * [ARKit 3](https://developer.apple.com/augmented-reality/arkit/) -  to implement plane detection and map the user's physical environment using the phone's camera, gyroscope and GPS system.
  * [SceneKit](https://developer.apple.com/scenekit/) - for generating the stars and planets' 3D models, wrapping them in textures, generating particle effects and placing the objects in space using nodes generated relative to the phone's position.
  * [UIKit](https://developer.apple.com/documentation/uikit) - to render the view on the user's phone and implement touch functionality/handle events.
  
* Testing frameworks:
  * [XCTest](https://developer.apple.com/documentation/xctest) - Apple's testing framework built into the Xcode SDK. Used to run unit tests and UI tests.
  * [Quick](https://github.com/Quick) and [Nimble](https://github.com/Quick/Nimble) - a pair of 3rd party testing/matcher frameworks used for running our initial tests, but eventually abandoned in favour of XCTest due to technical issues and time constraints.
  
* [Carthage](https://github.com/Carthage/Carthage) dependency manager.
  
* [In-The-Sky](https://in-the-sky.org/location.php) - a free online planetarium, we used this to calculate the positions of the stars and planets. By taking the right acension and declination of each object and placing them into a text file, we were able to program the View Controller to parse the data and place the objects in their correct positions relative to the users' location.

* iPhone running iOS 12.2.

## Improvements / Status

## Acknowledgements
Calum Darroch | Stuart Pethurst | Jose Quinones | Dominic White | Makers Academy
