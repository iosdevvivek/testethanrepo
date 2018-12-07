[https://github.com/iwasrobbed/Swift-CheatSheet#commenting]
#### button programatically
override func viewDidLoad() {
  super.viewDidLoad()

  let button = UIButton(frame: CGRect(x: 100, y: 100, width: 100, height: 50))
  button.backgroundColor = .green
  button.setTitle("Test Button", for: .normal)
  button.addTarget(self, action: #selector(buttonAction), for: .touchUpInside)

  self.view.addSubview(button)
}

@objc func buttonAction(sender: UIButton!) {
  print("Button tapped")
}

#### label programatically
- let label = UILabel(frame: CGRect(x: 0, y: 0, width: 200, height: 21))
label.center = CGPoint(x: 160, y: 285)
label.textAlignment = .center
label.text = "I'am a test label"
self.view.addSubview(label)

**Declaring Classes**

import UIKit

class MyClass {
    // Declare any constants or variables at the top
    let kRPErrorDomain = "com.myIncredibleApp.errors"
    var x: Int, y: Int

    // Use mark statements to logically organize your code

    // MARK: - Class Methods, e.g. MyClass.functionName()

    class func alert() {
        print("This is a class function.")
    }

    // MARK: - Instance Methods, e.g. myClass.functionName()

    init(x: Int, y: Int) {
        self.x = x
        self.y = y
    }

    // MARK: - Private Methods

    private func pointLocation() -> String {
        return "x: \(x), y: \(y)"
    }
}

