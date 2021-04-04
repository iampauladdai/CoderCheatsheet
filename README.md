# SwiftUI Cheatsheet

| UIKit                        | SwiftUI     | Note                                                      |
| ---------------------------- | ----------- | --------------------------------------------------------- |
| ```UIViewController```       | ```View```  |                                                           |
| ```UITableViewController ``` | ```List	``` | You can also use ScrollView with LazyHStack or LazyVStack |


# SwiftUI controls and styling
## Text
### code

```swift
Text("Hello World")
```

### Styling
```swift
Text("Hello World")
  .bold()
  .italic()
  .underline()
  .lineLimit(2)

Text("Hamlet")
    .font(.title)

Text("by William Shakespeare")
    .font(.system(size: 12, weight: .light, design: .serif))
    .italic()

Text("To be, or not to be, that is the question:")
    .frame(width: 100)

Text("Brevity is the soul of wit.")
    .frame(width: 100)
    .lineLimit(1)

Text("Hello world!")
    .frame(width: 200, height: 30, alignment: .topLeading)
    .border(Color.gray)
```

## Label
### code


## Image
### code

```swift
    //load image
    Image("turtlerock")

    //make image resizable to fit screen
    .resizable()
    .scaledToFit()
    
    //create circle shape
    Image("turtlerock")
            .clipShape(Circle())

    //add gray stroke with shadow
    Image("turtlerock")
            .clipShape(Circle())
            .overlay(Circle().stroke(Color.gray, lineWidth: 4))
            .shadow(radius: 7)

    //add custom SF symbols
    Image(systemName: "SF Name")

    //add corner radius to Image
    .cornerRadius(5)

    //add border to Image
    .border(Color("colorName"), width: 20)

    //fill stack with layer
    .layerPriority(1)
   
```
### Button

```swift
   Button(action: {}){ }
```


### Must-know codes
```swift
    //add shadow
    .shadow(radius: 7)

    //set size (takes at least one parameter)
     .frame(width: 200, height: 30, alignment: .topLeading)
    //or
     .frame(minWidth: 200, idealWidth: 300,maxWidth: 400, minHeight: 30, idealHeight: 50, maxHeight: 60, alignment: .topLeading)
    
    //set position
     .offset(x: 20 y: -130)

    //padding
     .padding(.bottom, -130)

    //ignore safeArea
     .ignoresSafeArea(edges: .top)

    //draws a horizontal line as a divider
     Divider()

    //set forground color
    .foregroundColor(.secondary)

    //means a code can be changed
    @State

    //preview layout with specific size
    .previewLayout(.fixed(width: 300, height: 70))

    //view multiple preview screens
     Group { }

    //dark mode 😎
    .colorScheme(.dark)
    .background(Color.black)

    //align stack
    VStack(alignment: .leading){ }

    //pass state variable (works like "self.")
    $state_variable

    //corner background
    .background(RoundedRectangle(cornerRadius: 8)
    .foregroundColor(.white)
    .shadow(color: Color("Shadow"), radius: 8, x: 0, y: 4))
```