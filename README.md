
# Rapport

**Skriv din rapport här!**

_Du kan ta bort all text som finns sedan tidigare_.

## Följande grundsyn gäller dugga-svar:

Ändrade namnet på appen genom att ändra "app_name" till Daniels App.
La till android permission för internet acces i AndroidManifest.xml.
I activity_main.xml tog jag bort Textview:n som fanns och skapade en WebView samt gav den ett id.
Gjorde en privat variabel myWebView och med hjälp av void onCreate la jag in
Koden som loadar den till his.se och WebViewClient som gör att vi kan browsa.
Enable:ade JavaScript execution och att den länkas till webbsettings.
Skapade en html sida genom att skapa en asset genom "app" och sedan en file döpt "DanielsApp.html"
La in så att external och internal laddar his.se och även kallat på dom i menyn. Tog tillbaka
toolbaren för att få alternativet.

```
<resources>
    <string name="app_name">Daniels App</string>
    <string name="action_external_web">External Web Page</string>
    <string name="action_internal_web">Internal Web Page</string>
</resources>


<uses-permission android:name="android.permission.INTERNET" />

    <WebView
        android:id="@+id/my_webview"
        android:layout_width="match_parent"
        android:layout_height="match_parent" />
        
        private WebView myWebView;
        
            @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        myWebView = findViewById(R.id.my_webview);
        myWebView.setWebViewClient(new WebViewClient()); // Do not open in Chrome!
        myWebView.loadUrl("https://his.se");
        
        private WebSettings webSettings;
        
                WebSettings webSettings = myWebView.getSettings();
        webSettings.setJavaScriptEnabled(true);
        
        showExternalWebPage();
        showInternalWebPage();
        
        
```

Bilder läggs i samma mapp som markdown-filen.

![](android.png)

Läs gärna:

- Boulos, M.N.K., Warren, J., Gong, J. & Yue, P. (2010) Web GIS in practice VIII: HTML5 and the canvas element for interactive online mapping. International journal of health geographics 9, 14. Shin, Y. &
- Wunsche, B.C. (2013) A smartphone-based golf simulation exercise game for supporting arthritis patients. 2013 28th International Conference of Image and Vision Computing New Zealand (IVCNZ), IEEE, pp. 459–464.
- Wohlin, C., Runeson, P., Höst, M., Ohlsson, M.C., Regnell, B., Wesslén, A. (2012) Experimentation in Software Engineering, Berlin, Heidelberg: Springer Berlin Heidelberg.
