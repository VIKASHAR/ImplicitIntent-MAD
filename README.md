# Ex.No:3a Develop program to create a text field and a button “Navigate”. When you enter “www.gmail.com” and press navigate button it should open google page using Implicit Intents.


## AIM:

To create a navigate button using Implicit Intent to display the gmail page using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as ImplicitIntent and click Next.

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Display message give in MainActivity file.

Step 7: Save and run the application.


## PROGRAM:
```
/*
Program to print the text “Implicitintent”.
Developed by: Vikash.A.R
Registeration Number : 212222040179
*/
```

## In activity_main.xml

    <?xml version="1.0" encoding="utf-8"?>
    <androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
        xmlns:app="http://schemas.android.com/apk/res-auto"
        xmlns:tools="http://schemas.android.com/tools"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        tools:context=".MainActivity">
    
        <EditText
            android:id="@+id/editText"
            android:layout_width="322dp"
            android:layout_height="71dp"
            android:layout_marginBottom="132dp"
            android:hint="Enter the URL"
            android:textSize="24sp"
            app:layout_constraintBottom_toTopOf="@+id/btn"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintHorizontal_bias="0.494"
            app:layout_constraintStart_toStartOf="parent" />
    
        <Button
            android:id="@+id/btn"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_marginBottom="172dp"
            android:onClick="search"
            android:text="Search"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintStart_toStartOf="parent" />
    
        <TextView
            android:id="@+id/textView"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Implicit Intent"
            android:textSize="48sp"
            app:layout_constraintBottom_toTopOf="@+id/editText"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintTop_toTopOf="parent"
            app:layout_constraintVertical_bias="0.576" />
    
    
    </androidx.constraintlayout.widget.ConstraintLayout>

## In MainActivity.java

    package com.example.implicit;
    
    import androidx.appcompat.app.AppCompatActivity;
    import android.content.Intent;
    import android.net.Uri;
    import android.os.Bundle;
    import android.view.View;
    import android.widget.Button;
    import android.widget.EditText;
    
    
    
    public class MainActivity extends AppCompatActivity {
    
        @Override
        protected void onCreate(Bundle savedInstanceState) {
    
            EditText editText;
            Button button;
    
            super.onCreate(savedInstanceState);
            setContentView(R.layout.activity_main);
    
            button = findViewById(R.id.btn);
            editText = (EditText) findViewById(R.id.editText);
    
            button.setOnClickListener(new View.OnClickListener() {
                @Override
                public void onClick(View view) {
                    String url=editText.getText().toString();
                    Intent intent = new Intent(Intent.ACTION_VIEW, Uri.parse(url));
                    startActivity(intent);
                }
            });
        }
    }


## OUTPUT

![WhatsApp Image 2024-03-14 at 08 43 02_e8a0c392](https://github.com/VIKASHAR/ImplicitIntent-MAD/assets/119405655/5698651a-43d1-4dd6-a1cb-61c34de82876)
![WhatsApp Image 2024-03-14 at 08 43 01_f8b0ac48](https://github.com/VIKASHAR/ImplicitIntent-MAD/assets/119405655/24bf083f-fc93-4c29-b476-9640462a37b6)
![WhatsApp Image 2024-03-14 at 08 43 01_56286177](https://github.com/VIKASHAR/ImplicitIntent-MAD/assets/119405655/8b800590-2098-453a-b6a5-b8242d5302f1)





## RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the gmail page using Android Studio is developed and executed successfully.


