# Cab Management System SalesForce-Project

#How to Use
Using this is pretty simple. You'll need to make 4 objects from your side and make some fields in all the objects (would hardly take an hour).
Since this project heavily uses Standard Objects from SalesForce, you won't have to specify objects on each and every page. Most of the work is being done on `Account` Object.
I'll post an image to all the objects and their fields in description as soon as I get the time, so everyone knows which object is being used.
All you need to do is, copy the codes from respective folders and just make some little changes here and there (if you want).

#File Naming
I've organised all the pages, classes and triggers in respective folders with proper extension. The code is well indented, it won't be highlighted on GitHub, because it doesn't support this SalesForce yet, I guess.
File Naming is pretty simple and straightforward, so there shouldn't be a problem. However, in trigger, I followed a special naming pattern.
For example : `Lead_To_Customers (Lead)`

This says that name of trigger is "`Lead_To_Customers`" and it is being activated on "`Lead`".

Anything with the `(Inactive)` tag in it means that it is not being used anywhere. It is not properly working and might be used in future with some updation.

Rest is self-explanatory!

#How does this work?

First, you'll need to update the source code of the VisualForce Pages and Classes, because I did not use partial links when I wrote this. So, update the links in classes as well, because of the PageReference method for page redirection.

Anyways, the basic working of this project is that :

The user will sign up from the sign up page and that data will be saved in a custom object with API name "`Customer__c`". Now, if the data is valid, it'll redirect the user to `Booking Page`, otherwise, it'll refresh the page and show the respective error. The `Email Address` field is Unique, so no repeated records for an email ID. Now, whatever you enter in booking page, it'll go and save in `Account`, a standard object. and a trigger will be activated when this runs, which will check the entered phone number and fetch the related email ID from the `Customer__c` into `Account`. And another trigger will be fired after insertion, that will copy the Phone Number from Ph_Num field of account an add it into the `Name` field of `Account` Object.
Now, after Booking, you'll see a thank you page and an email will be sent to the registered email ID with the billing details.


There's no driver's scenario, that is why the trip ends as soon as it starts. We'll probably work on this and make something out of it for driver, so the driver can end the trip status and some other things happen and it gets the job done.

Anyway, the project is very basic and does what it is intereded to do without any kind of problem(s).

Btw, there's a login functionality and password reset functionality, which is done via apex class. Look for it in the code itself ;




