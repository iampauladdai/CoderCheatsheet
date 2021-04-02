# SwiftUI Cheatsheet

|  UIKit  |    SwiftUI    | Note |
|-------|--------|-------|
| ```UIViewController``` |	```View``` | |
|```UITableViewController ```|	```List	```| You can also use ScrollView with LazyHStack or LazyVStack |


# SwiftUI controls and styling
## Text / Label
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
```
