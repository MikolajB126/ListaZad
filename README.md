<?xml version="1.0" encoding="utf-8"?>
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

        <!-- 🔹 Nowy przycisk USUŃ -->
        <Button
            android:id="@+id/buttonDelete"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_marginStart="8dp"
            android:background="@drawable/button_crimson"
            android:text="USUŃ"
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
