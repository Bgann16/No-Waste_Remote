# No Waste

### Welcome to No Waste! This is a SwiftUI app focused on promoting waste management and sustainability. The app educates users on how to save what's typically considered unusable.

# Features

* User Authentication: Securely log in and sign up via Auth0.
* Dynamic UI: The app uses device motion to create a dynamic, responsive interface.
* Dark Mode: A theme that switches according to the user's system preference.

# Prerequisites

Before you begin, ensure you have met the following requirements:

* Swift: This project is written in Swift and requires Xcode to run.

* Auth0: You'll need an Auth0 account and set up an application to handle authentication.
 
# Installation

Clone the project:

` bash
Copy code
git clone https://github.com/Bgann16/No-Waste_Remote.git `

Navigate to the project directory:

` bash
Copy code
cd No-Waste_Remote`

Open the project in Xcode: 

`bash
Copy code
open No\ Waste.xcodeproj/`

# Usage

After opening the project in Xcode, run the app in the simulator or on a real device.

## User Authentication

The app uses Auth0 for user authentication. To log in, tap the "Login" button. New users can sign up by tapping the "Signup" link.

swift
Copy code
`Auth0.webAuth().start { result in
    switch result {
    case .success(let credentials):
        // Handle successful login/signup
    case .failure(let error):
        // Handle error
    }
}`

# Motion-Based UI  
The app UI responds to device motion, providing a dynamic user experience. It uses the Core Motion framework to achieve this.

swift
Copy code
`self.motionManager.startAccelerometerUpdates(to: OperationQueue.current!) { (data, error) in
    if let accelerometerData = data {
        self.xAcceleration = accelerometerData.acceleration.x
    }
}`

# Themes
The app supports both light and dark mode, adapting to the system's appearance settings. This is achieved using SwiftUI's @Environment property wrapper.

swift
Copy code
`@Environment(\.theme) var theme`

# Support

If you encounter any issues or have questions, please open an issue on GitHub.

# Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.this is how it looks and the looks of it on the preview don't look the same how do I Mae it look the same
