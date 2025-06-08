# 📱 Stackroot Android App

A simple, secure, and mobile-friendly Android WebView container for the **Stackroot Solutions** platform — bringing the web experience to native Android devices using Java.

---

## 🚀 Features

- 🌐 Displays the Stackroot website in a WebView
- 🔒 Secure and optimized WebView settings
- 📲 Smooth back navigation handling
- ⚠️ Fallback for no internet connection
- 📱 Supports Android 5.0 (Lollipop) and above

---

## 🛠️ Built With

- Java
- Android SDK
- WebView

---

## 📦 Getting Started

### Clone the Repository


git clone https://github.com/your-username/stackroot-android-app.git
Open in Android Studio
Open the project folder in Android Studio

Let Gradle sync automatically

Connect your device or start an emulator

Click Run ▶️

📂 Project Structure
```bash
📁 stackroot-android-app/
├── 📁 app/
│   └── java/.../MainActivity.java
│   └── res/layout/activity_main.xml
├── AndroidManifest.xml
└── README.md
```

🧾 Code Snippets
----
MainActivity.java

```bash
import android.os.Bundle;
import android.webkit.WebSettings;
import android.webkit.WebView;
import android.webkit.WebViewClient;
import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    private WebView myWebView;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        myWebView = findViewById(R.id.webview);
        myWebView.setWebViewClient(new WebViewClient());
        WebSettings webSettings = myWebView.getSettings();
        webSettings.setJavaScriptEnabled(true);

        myWebView.loadUrl("https://stackrootsolutions.com/");
    }

    @Override
    public void onBackPressed() {
        if (myWebView.canGoBack()) {
            myWebView.goBack();
        } else {
            super.onBackPressed();
        }
    }
}
```

activity_main.xml
```bash
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent">

    <WebView
        android:id="@+id/webview"
        android:layout_width="match_parent"
        android:layout_height="match_parent" />
</RelativeLayout>
```
---

## 👨‍💻 Developer
Muhammad Abdullah Asif
🌐 abdullahasif.net
🌐 stackrootsolutions.com
📧 info@stackrootsolutions.com

📄 License
This project is licensed under the MIT License. See the LICENSE file for details.

💬 Feedback & Contributions
Pull requests, issues, and suggestions are welcome!
Feel free to open an Issue or fork the repo and contribute.
