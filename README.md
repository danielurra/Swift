# Swift
Swift is a new programming language developed by Apple that was released to developers at WWDC 2014.</br>
Swift can be used to develop applications for Apple’s iOS and OS X platforms.</br>
It is designed to work with, but eventually replace, Objective-C, the language originally used for developing applications on Apple’s platforms.</br>
Swift it's considered a protocol-oriented programming, it make use of various architectures to structure a complete iOS/OS X app.</br>
![Swift_logo](https://github.com/danielurra/Swift/assets/51704179/a211c946-ee31-4413-951e-f9019b7ab276)</br>
Xcode is Apple’s IDE, their main development tool, that will allows you to discover the Cocoa framework.</br>
Cocoa’s event-driven design Communicate with C and Objective-C.</br>
Thanks to polymorphism, you can take advantage of subclasses to add power and customization to existing classes.</br>
This is important particularly in the world of iOS programming, where most of the classes are defined by Cocoa and don’t belong to you.</br>
## Hello World!
```swift
import SwiftUI

struct ContentView: View {
    var body: some View {
        VStack {
            Image(systemName: "globe")
                .imageScale(.large)
                .foregroundColor(.accentColor)
            Text("Hello, Swift UI!")
        }
    }
}

```
## Swift Playground
[Swift-Playgrounds](https://github.com/danielurra/Swift/assets/51704179/c37ab536-b319-475e-8b4c-9c8deec730b6)</b>
## Swift UI - example
```swift
import SwiftUI
import Kingfisher
struct ContactGuestView: View {
    let name: String
    let pictureURL: URL?
    @State private var isInvited = false
    var body: some View {
        HStack(alignment: .center,
               spacing: 8.0) {
            KFImage(pictureURL)
                .resizable()
                .aspectRatio(contentMode: .fill)
                .frame(width: 32, height: 32)
                .clipShape(Circle())
            Toggle(name, isOn: $isInvited)
                .onChange(of: isInvited) { newValue in
                    print(newValue)
                }
                .font(.system(size: 16))
                .foregroundColor(.primary)
        }
       .padding(.leading, 16)
       .padding(.trailing, 16)
       .frame(height: 32, alignment: .center)
    }
}
struct ContactGuestView_Previews: PreviewProvider {
    static var previews: some View {
        ContactGuestView(
            name: "John Doe",
            pictureURL: URL(string: "https://picsum.photos/32/32")
        )
    }
}
```


