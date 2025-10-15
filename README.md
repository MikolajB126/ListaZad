dodaj usuwanie : <?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="8dp"
    tools:context=".MainActivity">

    <TextView
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:background="#6200EE"
        android:gravity="center"
        android:padding="12dp"
        android:text="listaAndr"
        android:textColor="#FFFFFF"
        android:textSize="18sp"
        android:textStyle="bold" />

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="horizontal"
        android:padding="8dp">

        <EditText
            android:id="@+id/editTextNewItem"
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            android:hint="Nowy element"
            android:inputType="text"
            android:minHeight="48dp" />

        <Button
            android:id="@+id/buttonAdd"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_marginStart="8dp"
            android:background="@drawable/button_crimson"
            android:text="DODAJ"
            android:textColor="#FFFFFF" />

    </LinearLayout>

    <ListView
        android:id="@+id/listViewNotes"
        android:layout_width="match_parent"
        android:layout_height="0dp"
        android:layout_weight="1"
        android:divider="#DC143C"
        android:dividerHeight="1dp" />
</LinearLayout>
package com.example.listazad;

import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.ArrayAdapter;
import android.widget.Button;
import android.widget.EditText;
import android.widget.ListView;
import java.util.ArrayList;

public class MainActivity extends AppCompatActivity {

    EditText editTextNewItem;
    Button buttonAdd;
    ListView listViewNotes;
    ArrayList<String> notes;
    ArrayAdapter<String> adapter;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        editTextNewItem = findViewById(R.id.editTextNewItem);
        buttonAdd = findViewById(R.id.buttonAdd);
        listViewNotes = findViewById(R.id.listViewNotes);

        notes = new ArrayList<>();
        notes.add("Zakupy: chleb, masło, ser");
        notes.add("Do zrobienia: obiad, umyć podłogi");
        notes.add("Weekend: kino, spacer z psem");

        adapter = new ArrayAdapter<>(this, android.R.layout.simple_list_item_1, notes);
        listViewNotes.setAdapter(adapter);

        buttonAdd.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                String newItem = editTextNewItem.getText().toString().trim();
                if (!newItem.isEmpty()) {
                    notes.add(newItem);
                    adapter.notifyDataSetChanged();
                    editTextNewItem.setText("");
                }
            }
        });
    }
}
