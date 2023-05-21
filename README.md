# Ex.No:3 Develop program to create a text field and a button “Navigate”. When you enter “www.google.com” and press navigate button it should open google page using Implicit Intents.


## AIM:

To create a navigate button using Implicit Intent to display the google page using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:

Step 1: Open Android Studio and then click on File -> New -> New project.
Step 2: Then type the Application name and click Next. 
Step 3: Then select the Minimum SDK as shown below and click Next.
Step 4: Then select the Empty Activity and click Next. Finally click Finish.
Step 5: Design layout in activity_main.xml
Step 6: Display message give in MainActivity file.
Step 7: Save and run the application.



## PROGRAM:
```
/*
Program to print the text “Implicitintent”.
Developed by: SMRITI.B
Registeration Number : 212221040156
*/
```
## activity_main.xml:
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">
    <Button
        android:id="@+id/button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginEnd="50dp"
        android:text="NAVIGATE"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.319" />
    <EditText
        android:id="@+id/editTextTextRedirecting"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginStart="35dp"
        android:ems="10"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.218" />
</androidx.constraintlayout.widget.ConstraintLayout>
```
## MainActivity.java:
```
package com.example.implicitintent;

import android.annotation.SuppressLint;
import android.content.Intent;
import android.net.Uri;
import android.os.Bundle;
import android.widget.Button;
import android.widget.EditText;

import androidx.appcompat.app.AppCompatActivity;
public class MainActivity extends AppCompatActivity {
        Button button;
        EditText editText;
        @SuppressLint("MissingInflatedId")
        @Override
        protected void onCreate(Bundle savedInstanceState) {
            super.onCreate(savedInstanceState);
            setContentView(R.layout.activity_main);
            button = findViewById(R.id.button);
            editText = findViewById(R.id.editTextTextRedirecting);
            button.setOnClickListener(view -> {
                String url=editText.getText().toString();
                Intent intent=new Intent(Intent.ACTION_VIEW, Uri.parse(url));
                startActivity(intent);
            });
    }
}
```
## OUTPUT
```
![OUTPUT1](https://github.com/smriti1910/NAVIGATE_BUTTON/assets/133334803/28f96b57-aa8b-4500-bb28-f47270273245)
![OUTPUT2](https://github.com/smriti1910/NAVIGATE_BUTTON/assets/133334803/1e9e9ad8-ec2b-4310-8f86-9936ab6dbdf5)
![INITIAL OUTPUT](https://github.com/smriti1910/NAVIGATE_BUTTON/assets/133334803/501195a5-afb9-4391-93b4-3641a561bf7f)
![NAVIGATED PAGE OUTPUT](https://github.com/smriti1910/NAVIGATE_BUTTON/assets/133334803/39391432-533c-4dad-aa65-07add24493e2)

```



## RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the google page using Android Studio is developed and executed successfully.

