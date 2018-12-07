# testethanrepo
# swift
## swift1
### swift3
*This text will be italic*
_This will also be italic_
**This text will be bold**
__This will also be bold__
_You **can** combine them_
unordered
* Item 1
* Item 2
  * Item 2a
  * Item 2b
  ordered
  1. Item 1
1. Item 2
1. Item 3
   1. Item 3a
   1. Item 3b
   
   First Header | Second Header
------------ | -------------
Content from cell 1 | Content from cell 2
Content in the first column | Content in the second column
   Links
   http://github.com - automatic!
[GitHub](http://github.com)
Blockquotes:
As Kanye West said:

> We're living the future so
> the present is our past.
In line code:
I think you should use an
`<addr>` element here instead.

What is the difference between Delegate and KVO?
*[www.google.com]
*[https://github.com/dashvlas/awesome-ios-interview/blob/master/Resources/English.md#integration-tests]
* test
1.test
2.test

import UIKit
import Foundation

class InterviewTest {
 var name: String
 lazy var greeting : String = { [unowned self] in
   return “Hello \(self.name)”
 }()
 
 init(name: String) {
  self.name = name
 }
}

let testObj = InterviewTest(name:”abhi”)
testObj.greeting
Note: Remember, the point of lazy properties is that they are computed only when they are first needed, after which their value is saved. So, if you call the iOSResumeDescription for the second time, the previously saved value is returned.
=======================================
override func viewDidLoad() {
  super.viewDidLoad()

  let button = UIButton(frame: CGRect(x: 100, y: 100, width: 100, height: 50))
  button.backgroundColor = .greenColor()
  button.setTitle("Test Button", forState: .Normal)
  button.addTarget(self, action: #selector(buttonAction), forControlEvents: .TouchUpInside)

  self.view.addSubview(button)
}

func buttonAction(sender: UIButton!) {
  print("Button tapped")
}
==================

