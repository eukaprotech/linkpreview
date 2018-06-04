# Description
An android asynchronous preview of a webpage from its link.

# Getting Started
Add the dependency in build.gradle (App module)

```compile 'com.eukaprotech.linkpreview:linkpreview:1.0.0@aar'```

Add permission in manifest file

```<uses-permission android:name="android.permission.INTERNET" />```

# Usage Example

        LinkPreview linkPreview = new LinkPreview(context);
        String link = "the web page complete link";
        linkPreview.preview(link, new LinkPreviewHandler() {

            @Override
            public void onStart() {
                
            }

            @Override
            public void onGetLinkRedirectedTo(String link_redirected_to) {
                
            }

            @Override
            public void onGetTitle(String title) {
                
            }

            @Override
            public void onGetDescription(String description) {
                
            }

            @Override
            public void onGetFavicon(String faviconLink) {
                
            }

            @Override
            public void onGetImageLink(String imageLink) {
                
            }

            @Override
            public void onFail(String response, String error) {
                
            }


            @Override
            public void onComplete() {
                
            }
        });
        
By default, the necessary preview content of the web page is stored to cache for faster later retrieval.

To skip reading from cache:

       linkPreview.skipReadFromCache(true);

To skip storing to cache:

       linkPreview.skipStoreToCache(true);
       
The below sample will avoid reading the contents of the previewed webpage from cache:

        LinkPreview linkPreview = new LinkPreview(context);
        String link = "the web page complete link";
        linkPreview.skipReadFromCache(true).preview(link, new LinkPreviewHandler() {

            @Override
            public void onStart() {
                
            }

            @Override
            public void onGetLinkRedirectedTo(String link_redirected_to) {
                
            }

            @Override
            public void onGetTitle(String title) {
                
            }

            @Override
            public void onGetDescription(String description) {
                
            }

            @Override
            public void onGetFavicon(String faviconLink) {
                
            }

            @Override
            public void onGetImageLink(String imageLink) {
                
            }

            @Override
            public void onFail(String response, String error) {
                
            }


            @Override
            public void onComplete() {
                
            }
        });
        
The entire cache, for all previewed web pages, is cleared with time.

To force the clearing of cache, use the static method:

       LinkPreview.clearCache(context);
       

[ ![Download](https://api.bintray.com/packages/eukaprotech/maven/linkpreview/images/download.svg?version=1.0.0) ](https://bintray.com/eukaprotech/maven/linkpreview/1.0.0/link)
