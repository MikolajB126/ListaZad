package com.example.listazad;

import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.AdapterView;
import android.widget.ArrayAdapter;
import android.widget.Button;
import android.widget.EditText;
import android.widget.ListView;
import android.widget.Toast;
import java.util.ArrayList;

public class MainActivity extends AppCompatActivity {

    EditText editTextNewItem;
    Button buttonAdd, buttonDelete;
    ListView listViewNotes;
    ArrayList<String> notes;
    ArrayAdapter<String> adapter;
    int selectedPosition = -1;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        editTextNewItem = findViewById(R.id.editTextNewItem);
        buttonAdd = findViewById(R.id.buttonAdd);
        buttonDelete = findViewById(R.id.buttonDelete);
        listViewNotes = findViewById(R.id.listViewNotes);

        notes = new ArrayList<>();
        notes.add("Zakupy: chleb, masło, ser");
        notes.add("Do zrobienia: obiad, umyć podłogi");
        notes.add("Weekend: kino, spacer z psem");

        adapter = new ArrayAdapter<>(this, android.R.layout.simple_list_item_activated_1, notes);
        listViewNotes.setAdapter(adapter);
        listViewNotes.setChoiceMode(ListView.CHOICE_MODE_SINGLE);

        listViewNotes.setOnItemClickListener(new AdapterView.OnItemClickListener() {
            @Override
            public void onItemClick(AdapterView<?> parent, View view, int position, long id) {
                selectedPosition = position;
            }
        });

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

        buttonDelete.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                if (selectedPosition != -1) {
                    String removed = notes.get(selectedPosition);
                    notes.remove(selectedPosition);
                    adapter.notifyDataSetChanged();
                    listViewNotes.clearChoices();
                    selectedPosition = -1;
                    Toast.makeText(MainActivity.this, "Usunięto: " + removed, Toast.LENGTH_SHORT).show();
                } else {
                    Toast.makeText(MainActivity.this, "Wybierz element do usunięcia", Toast.LENGTH_SHORT).show();
                }
            }
        });
    }
}
