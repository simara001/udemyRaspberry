## Actions: username and password

In this lesson we will cover:

* Start using UITextField (username and password)
* Select the correct Keyboards (for passwords)
* Select the correct Return button (Next, Go, Google it, etc)
* How to know the available delegate methods for UITextfield
* How to detect when the user is writing on a UITextField
* How to detect when the user pressed the Return button

#### Start using UITextField (username and password)

The first step would be to open the file *Main.storyboard*, locate your view, open the `Utilities` right panel, and explore the objects available. Drag and drop the *UITextField* on your view. You can explore all the attributes that can be customized (don't be shy about it). In this example we put a value of *Username* on the placeholder. In order to continue accessing the attributes of the `UITextField` we should link the graphic element to the code, by following the regular procedure. Open the `Assistant Editor`, put the Storyboard on one panel and the ViewController.h on the other one. Press *control* key on the keyboard, click and drag to the file. We named the `UITextField *textUsername` and you simply can access the text of it by calling its accessor: `self.textUsername.text`.


#### Select the correct Keyboards (for passwords)

Select the `UITextField` on the Storyboard and open the `Attribute Inspector`. Check the possibilities you have on the Keyboard and the Return button. Select the attribute you think is the best for your application. 

#### How to know the available delegate methods for UITextfield

We should start talking about delegates, the first step would be to tell the application that the `UITextField textUsername` will use its delegate to communicate actions associated with them. In order to do that, open the `Main.storyboard` file, select the `UITextField` and control drag it to the icon on the bottom of your View (`View Controller`) and click on *delegate*. After that, be sure to implement the `UITextFieldDelegate` protocol by putting the next line.

```objective-c
#import <UIKit/UIKit.h>

@interface ViewController : UIViewController <UITextFieldDelegate>

@property (weak, nonatomic) IBOutlet UITextField *textUsername;
@property (weak, nonatomic) IBOutlet UITextField *textPassword;

- (IBAction)buttonWasPressed:(id)sender;

@end
```

#### How to detect when the user pressed the Return button

You can access the `UITextField` class reference by pressing the *Command* key on your keyboard and clicking on `UITextField`. You can search for *Return* and you will see this reference:

```objective-c
- (BOOL)textFieldShouldReturn:(UITextField *)textField;              // called when 'return' key pressed. return NO to ignore.
```

We Will simply copy-paste that method on the `ViewController.m` and implement it. 

```objective-c
- (BOOL)textFieldShouldReturn:(UITextField *)textField {
    if (textField == self.textUsername) {
        NSLog(@"Username: %@", self.textUsername.text);
    } 
}
```
