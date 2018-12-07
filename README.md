   
**Interesting Links:**
  
* [https://github.com/dashvlas/awesome-ios-interview/blob/master/Resources/English.md#integration-tests]
 

 
 
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

