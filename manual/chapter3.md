## Connecting Graphic elements with code

In this lesson we will cover:

+ Add UIButton to the Storyboard
+ Connect UILabel to the ViewController.h
+ How to link UIButton to an action on the ViewController.m
+ Modify text of the UILabel by pressing a UIButton

#### Add UIButton to the Storyboard

Select the Storyboard, open the Utilities right bar, and find for *button* on the *Object Library* (the bottom panel on the Right Bar). Drag and drop the button to the Storyboard. You can customize it by openning the *Attribute Inspector* and changing what you consider is needed.

#### Connect UILabel to the ViewController.h

You may want to open the *Assistant Editor* by clicking the middle icon on the top right corner of XCode and make sure that on the left panel you have the Storyboard and on the right panel you have the ViewController.h file. Once you have that selected, press the key *control* from your keyboard, click on the Label and drag it to the ViewController.h file.

#### How to link UIButton to an action on the ViewController.m

You may want to open the *Assistant Editor* by clicking the middle icon on the top right corner of XCode and make sure that on the left panel you have the Storyboard and on the right panel you have the ViewController.h file. Once you have that selected, press the key *control* from your keyboard, click on the Button and drag it to the ViewController.h file. The only difference is that instead of *Outlet* you should select *Action*.

#### Modify text of the UILabel by pressing a UIButton

This is the main reason why you have `@property` on the ViewController.h before the `UILabel`. When you link an object (i.e. `@property (weak, nonatomic) IBOutlet UILabel *label`) a getter is automatically generated for you, which means, you can access all the attributes of the label directly on your code. Not only a getter is created, also a setter, so in this case, when you want to set the text of the label you can do it like this:

```objective-c
// Assuming buttonWasPressed is how you called
// the method when the button is Pressed
- (IBAction)buttonWasPressed:(id)sender {
    // Considering you have created a UILabel
    // named label
    self.label.text = @"Hello World";
}
```