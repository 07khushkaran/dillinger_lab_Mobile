
Practical 1: Android Development Environment: To study design aspects of
development environments like Android, iOS.

Android Development Environment

1. Programming Languages
● Java: The primary language for Android development for many years.
● Kotlin: Officially supported by Google and preferred for new Android applications
due to its modern features and interoperability with Java.
2. Integrated Development Environment (IDE)
● Android Studio: The official IDE for Android development, based on IntelliJ IDEA. It
includes features like code completion, debugging, and a powerful layout editor.
3. Software Development Kit (SDK)
● Android SDK: Provides the tools necessary to build, test, and debug Android
applications. Includes the Android emulator, platform tools, and various libraries.
4. Build System
● Gradle: The build automation tool used in Android Studio to compile, package, and
manage dependencies for Android projects.
5. Emulator
● Android Emulator: Part of the Android SDK, it allows developers to run and test
applications on virtual devices with different configurations and Android versions.
6. User Interface Design
● XML Layouts: UI components are typically defined in XML files.
● Jetpack Compose: A modern toolkit for building native UI using declarative
programming.
7. Frameworks and Libraries
● Android Jetpack: A set of libraries, tools, and guidance to help developers write
high-quality apps more easily. Includes components like LiveData, ViewModel,
Room, Navigation, and WorkManager.
8. Testing
● JUnit: For unit testing.
● Espresso: For UI testing.
● Robolectric: For running tests on the JVM without an emulator.
iOS Development Environment

1. Programming Languages
● Objective-C: An older language used for iOS development.
● Swift: The modern language for iOS development, designed to be safe, fast, and
expressive.
2. Integrated Development Environment (IDE)
● Xcode: The official IDE for iOS development, which includes a code editor,
debugger, and Interface Builder for designing user interfaces.
3. Software Development Kit (SDK)
● iOS SDK: Provides the necessary tools and frameworks for developing iOS
applications. Includes libraries like UIKit, Foundation, and Core Data.
4. Build System
● Xcode Build System: Integrated into Xcode for compiling, packaging, and managing
dependencies.
5. Simulator
● iOS Simulator: Allows developers to test and debug applications on virtual devices
with different iOS versions and device configurations.
6. User Interface Design
● Storyboard and XIB files: Interface Builder within Xcode is used to design UIs
visually.
● SwiftUI: A modern declarative framework for building UI across all Apple platforms.
7. Frameworks and Libraries
● Cocoa Touch: The application development environment for iOS, including
frameworks like UIKit, Foundation, and Core Graphics.
● Combine: A framework for handling asynchronous events by combining
event-processing operators.
8. Testing
● XCTest: For unit and UI testing.
● Quick/Nimble: Popular third-party frameworks for behavior-driven development
(BDD).
![image](https://github.com/user-attachments/assets/f76cdb1c-176e-4500-a6a6-ee9fb20ed76d)


Practical 2: Android Development Environment: To setup Android studio2
and study its basic components

Android Studio System Requirements for Windows

● Microsoft Windows 7/8/10 (32-bit or 64-bit)
● 4 GB RAM minimum, 8 GB RAM recommended (plus 1 GB for the Android
Emulator)
● 2 GB of available disk space minimum, 4 GB recommended (500 MB for IDE plus
1.5 GB for Android SDK and emulator system image)
● 1280 x 800 minimum screen resolution

Steps to Install Android Studio on Windows

● Step 1: Head over to this link to get the Android Studio executable or zip file.
● Step 2: Click on the Download Android Studio Button
● Step 3: After the downloading has finished, open the file from downloads and run it.
It will prompt the following dialog box.
● Step 4: It will start the installation, and once it is completed, it will be like the image
shown below.
● Step 5: Once “Finish” is clicked, it will ask whether the previous settings need to be
imported [if the android studio had been installed earlier], or not. It is better to choose
the ‘Don’t import Settings option’.
● Step 6: This will start the Android Studio.
Meanwhile, it will be finding the available SDK components.
● Step 7: After it has found the SDK components, it will redirect to the Welcome dialog
box.
Click on Next.
Choose Standard and click on Next. Now choose the theme, whether the Light theme or the
Dark one. The light one is called the IntelliJ theme whereas the dark theme is called Dracula.
Choose as required.
● Step 8: Now it is time to download the SDK components.
Click on Finish. Components begin to download let it complete.
The Android Studio has been successfully configured. Now it’s time to launch and build
apps. Click on the Finish button to launch it.
● Step 9: Click on Start a new Android Studio project to b

**Practical 3:** Android User Interface Design: To study various XML files needed
for interface design.

When designing the user interface (UI) for an Android application, several XML files are
typically used. These files define the layout, styles, strings, dimensions, and other aspects of
the UI. Here's an overview of the most common XML files:
1. Layout Files
Layout files define the structure and appearance of the UI components in an activity or
fragment.
● activity_main.xml: Defines the main layout for an activity.
● fragment_example.xml: Defines the layout for a fragment.
Common layout elements include:
● LinearLayout: Arranges its children in a single column or row.
● RelativeLayout: Positions its children relative to each other or to the parent.
● ConstraintLayout: Offers more flexibility and is recommended for complex layouts.
● FrameLayout: Designed to block out an area on the screen to display a single item.
Example of a simple layout file (activity_main.xml):
2. Resource Files
These files store various types of resources used in the app, such as strings, colors,
dimensions, and styles.
● strings.xml: Stores all the string resources used in the app.
● colors.xml: Defines the color resources.
● dimens.xml: Specifies dimension resources like padding and margins.
● styles.xml: Contains style definitions to maintain a consistent look and feel.
Example of strings.xml:
3. Manifest File
The AndroidManifest.xml file provides essential information about the app to the Android
system, including activities, permissions, services, and broadcast receivers.
Example of AndroidManifest.xml:
4. Drawable Resources
Drawable resources are graphics that can be drawn to the screen. These can be defined as
XML files (e.g., shapes, colors, state lists) or as image files (e.g., PNG, JPEG).
Example of a shape drawable (res/drawable/rounded_button.xml):
5. Menu Resources
Menu resource files define the contents of app menus.
Example of a menu resource (res/menu/menu_main.xml):
6. Values Resources
In addition to strings, colors, and dimensions, the values folder can contain other types of
resources:
● bools.xml: Stores boolean resources.
● integers.xml: Stores integer resources.
● arrays.xml: Defines array resources.
Example of arrays.xml:
These XML files collectively define the visual and interactive aspects of an Android
application's user interface. Understanding and effectively utilizing these files is crucial for
creating well-structured and maintainable Android apps.
Practical 4
Android User Interface Design: To implement different type of layouts like relative, grid,
linear and table.
i. Develop a program to implement constraint layout to display Hello World on screen.
Code:
//Activity_main.xml
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout
xmlns:android="http://schemas.android.com/apk/res/android"
xmlns:app="http://schemas.android.com/apk/res-auto"
android:layout_width="match_parent"
android:layout_height="match_parent">
<!-- TextView for "Hello World" -->
<TextView
android:id="@+id/helloWorldText"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:text="Hello World"
android:textSize="24sp"
android:textColor="#000000"
app:layout_constraintTop_toTopOf="parent"
app:layout_constraintBottom_toBottomOf="parent"
app:layout_constraintStart_toStartOf="parent"
app:layout_constraintEnd_toEndOf="parent" />
</androidx.constraintlayout.widget.ConstraintLayout>
// MainActivity.java
package com.example.practical1helloworld;
import android.os.Bundle;
import androidx.appcompat.app.AppCompatActivity;
public class MainActivity extends AppCompatActivity {
@Override
protected void onCreate(Bundle savedInstanceState) {
super.onCreate(savedInstanceState);
setContentView(R.layout.activity_main);
}
}
Output:
ii. Develop a program to implement linear layout to display send message and
registration form (vertical).
Code:
//activity_main.xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout
xmlns:android="http://schemas.android.com/apk/res/android"
android:layout_width="match_parent"
android:layout_height="match_parent"
android:orientation="vertical"
android:padding="16dp">
<!-- To Field -->
<EditText
android:layout_width="match_parent"
android:layout_height="wrap_content"
android:hint="To" />
<!-- Subject Field -->
<EditText
android:layout_width="match_parent"
android:layout_height="wrap_content"
android:hint="Subject"
android:layout_marginTop="16dp" />
<!-- Message Field -->
<EditText
android:layout_width="match_parent"
android:layout_height="wrap_content"
android:hint="Message"
android:inputType="textMultiLine"
android:minLines="4"
android:layout_marginTop="16dp" />
<!-- Send Button -->
<Button
android:id="@+id/button_send"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:text="SEND"
android:layout_gravity="end"
android:layout_marginTop="16dp" />
</LinearLayout>
//MainActivity.java
package com.example.practical2;
import android.os.Bundle;
import android.widget.Button;
import android.widget.Toast;
import androidx.appcompat.app.AppCompatActivity;
public class MainActivity extends AppCompatActivity {
@Override
protected void onCreate(Bundle savedInstanceState) {
super.onCreate(savedInstanceState);
setContentView(R.layout.activity_main); // Load the send message form
Button sendButton = findViewById(R.id.button_send);
sendButton.setOnClickListener(v -> {
// Display a message when the "SEND" button is clicked
Toast.makeText(MainActivity.this, "Message Sent", Toast.LENGTH_SHORT).show();
});
}
}
Output:
iii. Develop a program to implement relative layout to display Login and sign up form.
Code:
//Activity_main.xml
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
android:layout_width="match_parent"
android:layout_height="match_parent">
<!-- Login Form -->
<EditText
android:id="@+id/edtUsername"
android:layout_width="match_parent"
android:layout_height="wrap_content"
android:hint="Username"
android:layout_marginTop="100dp"
android:padding="10dp"
android:inputType="textPersonName"/>
<EditText
android:id="@+id/edtPassword"
android:layout_width="match_parent"
android:layout_height="wrap_content"
android:hint="Password"
android:layout_below="@id/edtUsername"
android:layout_marginTop="20dp"
android:padding="10dp"
android:inputType="textPassword"/>
<Button
android:id="@+id/btnLogin"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:text="Login"
android:layout_below="@id/edtPassword"
android:layout_marginTop="20dp"
android:layout_centerHorizontal="true"/>
<!-- Sign Up Form -->
<TextView
android:id="@+id/txtSignUp"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:text="Don't have an account? Sign Up"
android:layout_below="@id/btnLogin"
android:layout_marginTop="30dp"
android:layout_centerHorizontal="true"
android:textColor="@android:color/holo_blue_dark"/>
</RelativeLayout>
Output:
//Activity_main.xml
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
android:layout_width="match_parent"
android:layout_height="match_parent"
android:padding="16dp">
<!-- Username EditText -->
<EditText
android:id="@+id/username"
android:layout_width="match_parent"
android:layout_height="48dp"
android:hint="Username"
android:inputType="textPersonName"
android:layout_alignParentTop="true"
android:layout_marginTop="40dp"/>
<!-- Email EditText -->
<EditText
android:id="@+id/email"
android:layout_width="match_parent"
android:layout_height="48dp"
android:hint="@string/email"
android:inputType="textEmailAddress"
android:layout_below="@id/username"
android:layout_marginTop="20dp"/>
<!-- Password EditText -->
<EditText
android:id="@+id/password"
android:layout_width="match_parent"
android:layout_height="48dp"
android:hint="Password"
android:inputType="textPassword"
android:layout_below="@id/email"
android:layout_marginTop="20dp"/>
<!-- Sign Up Button -->
<Button
android:id="@+id/signUpButton"
android:layout_width="match_parent"
android:layout_height="wrap_content"
android:text="Sign Up"
android:layout_below="@id/password"
android:layout_marginTop="30dp"/>
</RelativeLayout>
Output:
iv. Develop a program to implement table layout to display calculator.
Code:
//Activity_main.xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
xmlns:tools="http://schemas.android.com/tools"
android:layout_width="match_parent"
android:layout_height="match_parent"
android:orientation="vertical"
android:padding="16dp"
android:gravity="center">
<!-- Display Screen for the Calculator -->
<EditText
android:id="@+id/display"
android:layout_width="match_parent"
android:layout_height="wrap_content"
android:autofillHints=""
android:textSize="30sp"
android:inputType="none"
android:focusable="false"
android:gravity="end"
android:layout_marginBottom="20dp"
tools:ignore="LabelFor" />
<!-- TableLayout for Calculator Buttons -->
<TableLayout
android:layout_width="match_parent"
android:layout_height="wrap_content">
<!-- First Row -->
<TableRow style="?android:attr/buttonBarStyle">
<Button
android:id="@+id/button7"
style="?android:attr/buttonBarButtonStyle"
android:layout_width="0dp"
android:layout_height="wrap_content"
android:layout_weight="1"
android:text="@string/_7" />
<Button
android:id="@+id/button8"
style="?android:attr/buttonBarButtonStyle"
android:layout_width="0dp"
android:layout_height="wrap_content"
android:layout_weight="1"
android:text="@string/_8" />
<Button
android:id="@+id/button9"
style="?android:attr/buttonBarButtonStyle"
android:layout_width="0dp"
android:layout_height="wrap_content"
android:layout_weight="1"
android:text="@string/_9" />
<Button
android:id="@+id/buttonDiv"
style="?android:attr/buttonBarButtonStyle"
android:layout_width="0dp"
android:layout_height="wrap_content"
android:layout_weight="1"
android:text="@string/_h" />
</TableRow>
<!-- Second Row -->
<TableRow style="?android:attr/buttonBarStyle">
<Button
android:id="@+id/button4"
style="?android:attr/buttonBarButtonStyle"
android:layout_width="0dp"
android:layout_height="wrap_content"
android:layout_weight="1"
android:text="@string/_4" />
<Button
android:id="@+id/button5"
style="?android:attr/buttonBarButtonStyle"
android:layout_width="0dp"
android:layout_height="wrap_content"
android:layout_weight="1"
android:text="@string/_5" />
<Button
android:id="@+id/button6"
style="?android:attr/buttonBarButtonStyle"
android:layout_width="0dp"
android:layout_height="wrap_content"
android:layout_weight="1"
android:text="@string/_6" />
<Button
android:id="@+id/buttonMul"
style="?android:attr/buttonBarButtonStyle"
android:layout_width="0dp"
android:layout_height="wrap_content"
android:layout_weight="1"
android:text="@string/_k" />
</TableRow>
<!-- Third Row -->
<TableRow style="?android:attr/buttonBarStyle">
<Button
android:id="@+id/button1"
style="?android:attr/buttonBarButtonStyle"
android:layout_width="0dp"
android:layout_height="wrap_content"
android:layout_weight="1"
android:text="@string/_1" />
<Button
android:id="@+id/button2"
style="?android:attr/buttonBarButtonStyle"
android:layout_width="0dp"
android:layout_height="wrap_content"
android:layout_weight="1"
android:text="@string/_2" />
<Button
android:id="@+id/button3"
style="?android:attr/buttonBarButtonStyle"
android:layout_width="0dp"
android:layout_height="wrap_content"
android:layout_weight="1"
android:text="@string/_3" />
<Button
android:id="@+id/buttonSub"
style="?android:attr/buttonBarButtonStyle"
android:layout_width="0dp"
android:layout_height="wrap_content"
android:layout_weight="1"
android:text="@string/_l" />
</TableRow>
<!-- Fourth Row -->
<TableRow style="?android:attr/buttonBarStyle">
<Button
android:id="@+id/button0"
style="?android:attr/buttonBarButtonStyle"
android:layout_width="0dp"
android:layout_height="wrap_content"
android:layout_weight="1"
android:text="@string/_0" />
<Button
android:id="@+id/buttonClear"
style="?android:attr/buttonBarButtonStyle"
android:layout_width="0dp"
android:layout_height="wrap_content"
android:layout_weight="1"
android:text="@string/c" />
<Button
android:id="@+id/buttonEqual"
style="?android:attr/buttonBarButtonStyle"
android:layout_width="0dp"
android:layout_height="wrap_content"
android:layout_weight="1"
android:text="@string/p" />
<Button
android:id="@+id/buttonAdd"
style="?android:attr/buttonBarButtonStyle"
android:layout_width="0dp"
android:layout_height="wrap_content"
android:layout_weight="1"
android:text="@string/a" />
</TableRow>
</TableLayout>
</LinearLayout>
Output
