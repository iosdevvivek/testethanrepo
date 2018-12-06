# testethanrepo
test
What is the difference between Delegate and KVO?
Both are ways to have relationships between objects. Delegation is a one-to-one relationship where one object implements a delegate protocol and another uses it and sends messages to it, assuming that those methods are implemented since the receiver promised to comply to the protocol. KVO is a many-to-many relationship where one object could broadcast a message and one or multiple other objects can listen to it and react. KVO does not rely on protocols. KVO is the first step and the fundamental block of reactive programming (RxSwift, ReactiveCocoa, etc.)
Lazy Stored Property vs Stored Property
The closure associated to the lazy property is executed only if you read that property. So if for some reason that property is not used (maybe because of some decision of the user) you avoid unnecessary allocation and computation. You can populate a lazy property with the value of a stored property.

You can use self inside the closure of a lazy property. If you need to use self inside the function. In fact, if you're using a class rather than a structure, you should also declare [unowned self] inside your function so that you don't create a strong reference cycle(check the code below).

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
