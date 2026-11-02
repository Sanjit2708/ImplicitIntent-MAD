# Ex.No:2a Develop program to create a text field and a button “Navigate”. When you enter “www.gmail.com” and press navigate button it should open google page using Implicit Intents.


## AIM:

To create a navigate button using Implicit Intent to display the gmail page using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:

1. Create Layout – Add an EditText for URL input and a Button labeled "Navigate".
2. Initialize Components – Link EditText and Button with findViewById().
3. Set Listener – Attach onClickListener to the "Navigate" button.
4. Get Input – Read the text from EditText when button is clicked.
5. Create Intent – Use Intent.ACTION_VIEW with Uri.parse() of the entered URL.
6. Start Activity – Call startActivity(intent) to open the browser page.

## PROGRAM:
```
/*
Program to print the text “Implicitintent”.
Developed by: Sanjit A
Registration Number : 212224220087
*/
```

## MainActivity.java:
```
package com.example.muiex2a;

import android.content.Intent;
import android.net.Uri;
import android.os.Bundle;
import android.widget.Button;
import android.widget.EditText;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        EditText editText;
        Button button;
        button = findViewById(R.id.button);
        editText = findViewById(R.id.editText);

        button.setOnClickListener(view -> {
            String url = editText.getText().toString();
            Intent intent = new Intent(Intent.ACTION_VIEW, Uri.parse(url));
            startActivity(intent);
        });
    }
}
```

## activity_main.xml:
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:id="@+id/main"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <EditText
        android:id="@+id/editText"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:minHeight="48dp"
        android:autofillHints="uri"
        android:ems="10"
        android:hint="@string/enter_url"
        android:inputType="textUri"
        app:layout_constraintBottom_toTopOf="@+id/button"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.497"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.669" />

    <Button
        android:id="@+id/button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:minHeight="48dp"
        android:layout_marginBottom="272dp"
        android:text="@string/click_here"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.498"
        app:layout_constraintStart_toStartOf="parent" />

</androidx.constraintlayout.widget.ConstraintLayout>
```

## OUTPUT

## activity_main.xml:
<img width="1917" height="1090" alt="image" src="https://github.com/user-attachments/assets/e51761fd-2da1-4d50-9560-90b1f47081b3" />


## MainActivity.java:
<img width="1917" height="1136" alt="image" src="https://github.com/user-attachments/assets/f01899b6-0f21-4388-b3ee-3eb7e315d47c" />


## Implicit Intent:
<img width="1917" height="1136" alt="image" src="https://github.com/user-attachments/assets/76e08635-b4fa-4c38-9f8c-587be68341a2" />


## Navigation:

<img width="1917" height="1132" alt="image" src="https://github.com/user-attachments/assets/e85b8746-bf7f-476b-b39a-6c54c83eec8d" />





## RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the gmail page using Android Studio is developed and executed successfully.


