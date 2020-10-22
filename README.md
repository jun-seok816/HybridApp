# gps앱의 하이브리드 앱추가



# initializeWebView메소드

## Description 

- 자바스크립트에서 안드로이드 메소드를 인식할 수 있게 설정하는 메소드.
- 제공된 이름을 사용하여 자바스크립트에서 안드로이드 메소드에 엑세스 할 수 있습니다.
            
## Parameter

- 없음
    
## Return
- type : void

- value : 없음

## Dependence function

- getSettings()
  - WebView의 설정을 제어하는데 필요한 WebSettings 객체를 가져옵니다.
  - https://developer.android.com/reference/android/webkit/WebView#getSettings()

- addJavascriptInterface: 
  - 제공된 java객체를 webView에 삽입합니다. 
  - https://developer.android.com/reference/android/webkit/WebView

- setClickable(): 
  - 버튼을 활성화/비활성화시킬 수 있다

- setJavaScriptEnabled(true or falee): 
  - WebView에서 JavaScript실행을 사용하도록 지시합니다
  - https://developer.android.com/reference/android/webkit/WebSettings#setJavaScriptEnabled(boolean)
  
- setJavaScriptCanOpenWindowsAutomatically(true or false): 
  - 자동으로 창을 열도록 JavaScript에 지시합니다.
  - https://developer.android.com/reference/android/webkit/WebSettings#setJavaScriptCanOpenWindowsAutomatically(boolean)

- setAllowUniversalAccessFromFileURLs(true or false):
  - 파일 체계 URL의 Context에서 원본 간 요청이 다른 파일 체계 URL의 콘텐츠에 액세스 할 수 있도록 허용할지 여부를 설정합니다.
  - https://developer.android.com/reference/android/webkit/WebSettings#setAllowUniversalAccessFromFileURLs(boolean)

- setAllowFileAccessFromFileURLs(true or false): 
  - 파일 체계 URL의 Context에서 실행되는 Javascript가 모든 출처의 콘텐츠에 엑세스 할 수 있는지의 여부
  - https://developer.android.com/reference/android/webkit/WebSettings#setAllowFileAccessFromFileURLs(boolean)
  
- setBuiltInZoomControls(true or false): 
  - WebView가 내장 된 확대 / 축소 메커니즘을 사용해야하는지 여부를 설정합니다.
  - https://developer.android.com/reference/android/webkit/WebSettings#setBuiltInZoomControls(boolean)
  
- setSupportZoom(true or false): 
  - WebView가 화면 확대 / 축소 컨트롤 및 제스처를 사용하여 확대 / 축소를 지원해야하는지 여부를 설정합니다.
  - https://developer.android.com/reference/android/webkit/WebSettings#setSupportZoom(boolean)
  
- setLightTouchEnabled(true or false): 
  - 가벼운 터치를 사용하여 선택하고 마우스 오버를 활성화 할 수 있습니다.
  - https://developer.android.com/reference/android/webkit/WebSettings#setLightTouchEnabled(boolean)
  
- setDomStorageEnabled(true or false): 
  - DOM 저장소 API 사용 여부를 설정합니다.
  - https://developer.android.com/reference/android/webkit/WebSettings#setDomStorageEnabled(boolean)
  
- setPluginState(WebSettings.PluginState state): 
  - WebView에 요청시 플러그인을 활성화, 비활성화 또는 포함하도록 지시합니다
  - https://developer.android.com/reference/android/webkit/WebSettings#setPluginState(android.webkit.WebSettings.PluginState)
  
- setLoadWithOverviewMode(true or false):
  - WebView가 개요 모드에서 페이지를로드할지 여부를 설정합니다.즉, 콘텐츠를 너비별로 화면에 맞게 축소합니다.
  - https://developer.android.com/reference/android/webkit/WebSettings#setLoadWithOverviewMode(boolean)'
  
- setUseWideViewPort(true or false):
  - WebView가 "viewport"HTML 메타 태그에 대한 지원을 활성화해야하는지 아니면 와이드 뷰포트를 사용해야하는지 여부를 설정합니다.
  - https://developer.android.com/reference/android/webkit/WebSettings#setUseWideViewPort(boolean)
  
- setRenderPriority( WebSettings.RenderPriority): 
  - 렌더 스레드의 우선 순위를 설정합니다.
  - https://developer.android.com/reference/android/webkit/WebSettings#setRenderPriority(android.webkit.WebSettings.RenderPriority)
  
- setCacheMode(int mode): 
  - 캐시가 사용되는 방식을 재정의합니다. 
  - https://developer.android.com/reference/android/webkit/WebSettings#setPluginState(android.webkit.WebSettings.PluginState)


- setWebViewClient(): 
  - 다양한 알림과 요청을받을 WebViewClient를 설정합니다. 
  - https://developer.android.com/reference/android/webkit/WebView#setWebViewClient(android.webkit.WebViewClient)
  
- onPageStarted(): 
  - WebView에서 처음 한 번만 호출되는 메소드, 페이지 로딩이 시작된 것을 알립니다. 
  - https://developer.android.com/reference/android/webkit/WebViewClient#onPageStarted(android.webkit.WebView,%20java.lang.String,%20android.graphics.Bitmap)
  
- onPageFinished():
  - WebView에서 처음 한 번만 호출되는 메소드, 페이지 로딩이 완료된 것을 알립니다.
  - https://developer.android.com/reference/android/webkit/WebViewClient#onPageFinished(android.webkit.WebView,%20java.lang.String)
  
- shouldOverrideUrlLoading(): 
  - 새로운 URL이 현재 WebView에 로드되려고 할 때 호스트 응용 프로그램에게 컨트롤을 대신할 기회를 줍니다
  - https://developer.android.com/reference/android/webkit/WebViewClient#shouldOverrideUrlLoading(android.webkit.WebView,%20android.webkit.WebResourceRequest)
  
- onReceivedSslError():
  - SSL 오류를 무시할 때 쓰는 코드>https://aorica.tistory.com/103
  - https://developer.android.com/reference/android/webkit/WebViewClient#onReceivedSslError(android.webkit.WebView,%20android.webkit.SslErrorHandler,%20android.net.http.SslError)
  
- onReceivedError(): 
  - 호스트 응용 프로그램에게 오류를 보고합니다.
  - https://developer.android.com/reference/android/webkit/WebViewClient#onReceivedError(android.webkit.WebView,%20int,%20java.lang.String,%20java.lang.String)
  - http://ankyu.entersoft.kr/lecture/android/webview_02.asp
    
## Source code    
    
    ```
    @SuppressLint("JavascriptInterface")
    public void initializeWebView() {
        WebSettings webSettings = wv.getSettings();

        wv.addJavascriptInterface(new WebVCamBridgeInterface(), "AndroidDevice");
        wv.setClickable(true);
        webSettings.setJavaScriptEnabled(true);
        webSettings.setJavaScriptCanOpenWindowsAutomatically(true);
        webSettings.setAllowFileAccessFromFileURLs(true);
        webSettings.setAllowUniversalAccessFromFileURLs(true);
        webSettings.setBuiltInZoomControls(true);
        webSettings.setSupportZoom(true);
        webSettings.setLightTouchEnabled(true);
        webSettings.setDomStorageEnabled(true);
        webSettings.setPluginState(WebSettings.PluginState.ON);


        webSettings.setLoadWithOverviewMode(false);
        webSettings.setUseWideViewPort(false);


        webSettings.setRenderPriority(WebSettings.RenderPriority.HIGH);
        webSettings.setCacheMode(WebSettings.LOAD_NO_CACHE);

        wv.setWebViewClient(new WebViewClient() {
            @Override
            public void onPageStarted(WebView view, String url, Bitmap favicon) {
                super.onPageStarted(view, url, favicon);
            }

            @Override
            public void onPageFinished(WebView view, String url) {
                super.onPageFinished(view, url);

            }

            @Override
            public boolean shouldOverrideUrlLoading(WebView view, String url) {
                return super.shouldOverrideUrlLoading(view, url);
            }

            @Override
            public void onReceivedSslError(WebView view, SslErrorHandler handler, SslError error) {
                handler.proceed();
            }

            @Override
            public void onReceivedError(WebView view, int errorCode, String description, String failingUrl) {
                super.onReceivedError(view, errorCode, description, failingUrl);
            }

        });
    }
    ```
    
# ShowLocation메소드

## Description 

 - 자바스크립트에서 호출 할 수 있게 만든 메소드
 - 위도랑 경도를 변수에 초기화, 토스트 문으로 위도랑 경도를 띄워줌
            
## Parameter

- 없음
    
## Return 

 - type : void
 
 - value : 없음

## Dependence function

- getLatitude(): 위도를 리턴
  - https://developer.android.com/reference/android/location/Location#getLatitude()

- getLongitude(): 경도를 리턴
  - https://developer.android.com/reference/android/location/Location#getLongitude()

## Source code 
```
@JavascriptInterface
        public void ShowLocation() {
            gpsTracker = new GpsTracker(MainActivity.this);

            double latitude = gpsTracker.getLatitude();
            double longitude = gpsTracker.getLongitude();


            Toast.makeText(MainActivity.this, "현재위치 \n위도 " + latitude + "\n경도 " + longitude, Toast.LENGTH_LONG).show();
            }
```

# GetLocation메소드

## Description 

- 자바스크립트에서 호출 할 수 있게 만든 메소드

- String a를 얻어온다음 위도랑 경도를 덧씌워 초기화
            
## Parameter

- 없음
    
## Return

- type : String

- value : a

## Dependence function

- getLatitude(): 위도를 리턴
  - https://developer.android.com/reference/android/location/Location#getLatitude()

- getLongitude(): 경도를 리턴
  - https://developer.android.com/reference/android/location/Location#getLongitude()


## Source code 

```
@JavascriptInterface
        public String GetLocation(){
            gpsTracker = new GpsTracker(MainActivity.this);

            double latitude = gpsTracker.getLatitude();
            double longitude = gpsTracker.getLongitude();

            String a;
            a = "현재위치 \n위도 " + latitude + "\n경도 " + longitude;

            return a;

        }
```

# JavaScript

## Description 

자바스크립트가 안드로이드에 있는 함수를 호출

## Return value

Id가 'aa'인 P태그의 문장을 얻어온 String a의 내용으로 덧씌움.
ShowLocation()호출

## Js Source Code

```
function clickBtn(){
     var e = document.getElementById('aa');
     var c=AndroidDevice.GetLocation();
     e.innerHTML=c;
     AndroidDevice.ShowLocation();
  }
```

## Html Source Code

```
<!DOCTYPE html>
<head>
    <title></title>
</head>
<script src="index.js">
</script>
<body>
<center>
    <p><input type="button" value="GPS" onClick="clickBtn()"/></p>
    <h4 id="aa"></h4>
</center>
</body>
</html>
```

## Additional explanation

addJavascriptInterface메소드에서 제공된 문자열 이름 AndroidDevice을 통해서 자바스크립트에서 자바 객체의 메소드에 엑세스 할 수 있습니다.
이때 자바 객체의 메소드에는  @JavascriptInterface 주석이 달린 공용 메소드만 자바스크립트에서 엑세스 할 수 있습니다.
