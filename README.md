<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="16dp">

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="horizontal">

        <EditText
            android:id="@+id/editTextNewItem"
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            android:hint="Nowy element"
            android:inputType="text"
            android:layout_marginEnd="8dp" />

        <Button
            android:id="@+id/buttonAdd"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="DODAJ"
            android:background="#DC143C"
            android:textColor="#FFFFFF"
            android:paddingLeft="16dp"
            android:paddingRight="16dp" />
    </LinearLayout>

    <TextView
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Zakupy: chleb, masło, ser"
        android:paddingTop="12dp"
        android:textSize="16sp" />

    <TextView
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Do zrobienia: obiad, umyć podłogi"
        android:paddingTop="8dp"
        android:textSize="16sp" />

    <TextView
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Weekend: kino, spacer z psem"
        android:paddingTop="8dp"
        android:textSize="16sp" />

</LinearLayout>
