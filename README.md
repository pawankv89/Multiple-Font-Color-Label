
Multiple Font Color Label
=========

## Multiple Font Color Label.
------------
 Added Some screens here.
 
![](https://github.com/pawankv89/MultipleFontColorLabel/blob/master/Screens/1.png)

## Usage
------------
 iOS 9 Demo showing how to Multiple Font Color Label on iPhone X Simulator in  Objective-C.

```Swift

class ViewController: UIViewController {

@IBOutlet weak var Label1: UILabel!
@IBOutlet weak var Label2: UILabel!
@IBOutlet weak var Label3: UILabel!
@IBOutlet weak var Label4: UILabel!

override func viewDidLoad() {
super.viewDidLoad()
// Do any additional setup after loading the view, typically from a nib.

fontChange1()
fontChange2()
fontChange3()
fontChange4()
}

override func didReceiveMemoryWarning() {
super.didReceiveMemoryWarning()
// Dispose of any resources that can be recreated.
}

func fontChange1() -> Void {

let stringValue = "Pawan Kumar Sharma"
Label1.text = stringValue;
let attributedString: NSMutableAttributedString = NSMutableAttributedString(string: stringValue)
attributedString.setColorForText(textForAttribute: "pa", withColor: UIColor.black)
attributedString.setColorForText(textForAttribute: "kumar", withColor: UIColor.orange)
attributedString.setColorForText(textForAttribute: "shar", withColor: UIColor.red)
Label1.font = UIFont.boldSystemFont(ofSize: 30)

Label1.attributedText = attributedString

}
func fontChange2() -> Void {

let attrs0 = [NSAttributedStringKey.font : UIFont.boldSystemFont(ofSize: 15), NSAttributedStringKey.foregroundColor : UIColor.black]

let attrs1 = [NSAttributedStringKey.font : UIFont.boldSystemFont(ofSize: 12), NSAttributedStringKey.foregroundColor : UIColor.green]

let attrs2 = [NSAttributedStringKey.font : UIFont.boldSystemFont(ofSize: 18), NSAttributedStringKey.foregroundColor : UIColor.blue]

let attributedString = NSMutableAttributedString(string:"Pawan", attributes:attrs0)

let attributedString1 = NSMutableAttributedString(string:"Kumar", attributes:attrs1)

let attributedString2 = NSMutableAttributedString(string:"Sharma", attributes:attrs2)

attributedString.append(attributedString1)
attributedString.append(attributedString2)
Label2.attributedText = attributedString
}

func fontChange3() -> Void {

let attrs0 = [NSAttributedStringKey.font : UIFont.boldSystemFont(ofSize: 15), NSAttributedStringKey.backgroundColor : UIColor.black]

let attrs1 = [NSAttributedStringKey.font : UIFont.boldSystemFont(ofSize: 12), NSAttributedStringKey.backgroundColor : UIColor.green]

let attrs2 = [NSAttributedStringKey.font : UIFont.boldSystemFont(ofSize: 18), NSAttributedStringKey.backgroundColor : UIColor.blue]

let attributedString = NSMutableAttributedString(string:"Pawan", attributes:attrs0)

let attributedString1 = NSMutableAttributedString(string:"Kumar", attributes:attrs1)

let attributedString2 = NSMutableAttributedString(string:"Sharma", attributes:attrs2)

attributedString.append(attributedString1)
attributedString.append(attributedString2)
Label3.attributedText = attributedString

}
func fontChange4() -> Void {

let attrs0 = [NSAttributedStringKey.font : UIFont(name: "AvenirNext-Bold", size: 15)!, NSAttributedStringKey.foregroundColor : UIColor.black]

let attrs1 = [NSAttributedStringKey.font : UIFont(name: "AvenirNext-Bold", size: 20)!, NSAttributedStringKey.foregroundColor : UIColor.green, NSAttributedStringKey.underlineColor : UIColor.red, NSAttributedStringKey.underlineStyle: NSUnderlineStyle.styleSingle.rawValue] as [NSAttributedStringKey : Any]

let attrs2 = [NSAttributedStringKey.font : UIFont(name: "AvenirNext-Bold", size: 12)!, NSAttributedStringKey.foregroundColor : UIColor.blue, NSAttributedStringKey.underlineStyle: NSUnderlineStyle.styleSingle.rawValue] as [NSAttributedStringKey : Any]

let attributedString = NSMutableAttributedString(string:"Pawan", attributes:attrs0)

let attributedString1 = NSMutableAttributedString(string:"Kumar", attributes:attrs1)

let attributedString2 = NSMutableAttributedString(string:"Sharma", attributes:attrs2)

attributedString.append(attributedString1)
attributedString.append(attributedString2)
Label4.attributedText = attributedString
}

}

extension NSMutableAttributedString {

func setColorForText(textForAttribute: String, withColor color: UIColor) {
let range: NSRange = self.mutableString.range(of: textForAttribute, options: .caseInsensitive)
self.addAttribute(NSAttributedStringKey.foregroundColor, value: color, range: range)
}

}

```

```objective-c


```

```objective-c

```

## License

This code is distributed under the terms and conditions of the [MIT license](LICENSE).

## Change-log

A brief summary of each this release can be found in the [CHANGELOG](CHANGELOG.mdown). 
