<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:paddingTop="20dp"
    android:background="#FFFFFF"
    android:padding="20dp">

    <TextView
        android:id="@+id/tytul"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Domek w górach"
        android:textSize="24sp"
        android:textStyle="bold"
        android:textColor="#000000"
        android:layout_gravity="center" />

    <ImageView
        android:id="@+id/obraz"
        android:layout_width="match_parent"
        android:layout_height="200dp"
        android:src="@drawable/obraz"
        android:scaleType="centerCrop" />

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="horizontal"
        android:background="#008080"
        android:padding="10dp">

        <Button
            android:id="@+id/btn_polub"
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            android:text="POLUB"
            android:textColor="#FFFFFF"
            android:background="#008080"
            android:textStyle="bold" />

        <Button
            android:id="@+id/btn_usun"
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            android:text="USUŃ"
            android:textColor="#FFFFFF"
            android:background="#008080"
            android:textStyle="bold" />

        <Button
            android:id="@+id/btn_zapisz"
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            android:text="ZAPISZ"
            android:textColor="#FFFFFF"
            android:background="#008080"
            android:textStyle="bold" />
    </LinearLayout>

    <TextView
        android:id="@+id/liczba_polubien"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="0 polubień"
        android:textSize="16sp"
        android:gravity="end"
        android:textColor="#000000" />

    <View
        android:layout_width="match_parent"
        android:layout_height="1dp"
        android:background="#808080" />

    <TextView
        android:id="@+id/opis_tytul"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Opis"
        android:textSize="18sp"
        android:textStyle="bold"
        android:textColor="#000000" />

    <TextView
        android:id="@+id/opis_tresc"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Odwiedź komfortowy domek w Sudetach, blisko do szlaków turystycznych."
        android:textSize="14sp"
        android:textColor="#808080" />

</LinearLayout>
