## Gesture Recognizers

In this lesson we will cover:

* How to add *Gesture Recognizers*
* How to dismiss a keyboard on Tap
* Testing different types of *Gesture Recognizers*

#### How to add *Gesture Recognizers*

The first thing to do is to open the Storyboard, open the *Utilities* panel, search for *gesture* and then simply drag and drop the element on the top of the view. After that is finished, open the *Assistant Editor* and control drag and drop from your *Gesture Recognizer* to the ViewController.h. Make sure that you are dragging the *gesture* to the *.h file and not into the *.m one. 

Finally, instead of putting that *Gesture Recognizer* open the *Show Document Online* and then control drag and drop from your view to your *Gesture Recognizer*. Remember that you can see any associations to the elements on the Storyboard by selecting them and then selecting the *Connections Inspector* on the right panel (*Utilities*).

#### How to dismiss a keyboard on Tap

When the user selects a `UITextField`, it becomes the first responder. Apple's implementation states that it needs a keyboard, and so, the keyboard appears. When you want to dismiss the keyboard, your `UITextField` should `[myTextField resignFirstResponder]`. You can see the implementation of the code:

```objective-c
- (IBAction)tapWasRecognized:(id)sender {
    [self.textUsername resignFirstResponder];
    [self.textPassword resignFirstResponder];
}
```

In this case we only have 2 `UITextField`, if we have a situation where you have multiple *text fields* you will need to find the first responder, and the resign to that privilege.