/* Interface */
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout
   xmlns:android="http://schemas.android.com/apk/res/android"
   android:layout_width="match_parent"
   android:layout_height="match_parent"
   android:id="@+id/main"
   android:orientation="vertical"
   android:background="@drawable/fundo">


   <ImageView
       android:id="@+id/figura"
       android:layout_width="match_parent"
       android:layout_height="250dp" />
   <Button
       android:layout_width="match_parent"
       android:layout_height="wrap_content"
       android:text="Carro 1"
       android:textSize="30dp"
       android:layout_marginLeft="50dp"
       android:layout_marginRight="50dp"
       android:layout_marginTop="200dp"
       android:id="@+id/btCarro1"/>
   <Button
       android:layout_width="match_parent"
       android:layout_height="wrap_content"
       android:text="Carro 2"
       android:textSize="30dp"
       android:layout_marginLeft="50dp"
       android:layout_marginRight="50dp"
       android:id="@+id/btCarro2"/>
</LinearLayout>
/* Java part */
package com.example.n1_exemplo3;


import androidx.appcompat.app.AppCompatActivity;


import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.ImageView;


public class MainActivity extends AppCompatActivity {
   ImageView figura;
   Button    btCarro1,  btCarro2;


   @Override
   protected void onCreate(Bundle savedInstanceState) {
       super.onCreate(savedInstanceState);
       setContentView(R.layout.activity_main);


       figura   = findViewById(R.id.figura);
       btCarro1 = findViewById(R.id.btCarro1);
       btCarro2 = findViewById(R.id.btCarro2);


       btCarro1.setOnClickListener(new View.OnClickListener() {
           @Override
           public void onClick(View v) {
               figura.setImageResource(R.drawable.carro1);
           }
       });


       btCarro2.setOnClickListener(new View.OnClickListener() {
           @Override
           public void onClick(View v) {
               figura.setImageResource(R.drawable.carro2);
           }
       });




   }
}



