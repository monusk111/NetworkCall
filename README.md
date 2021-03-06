# NetworkCall

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)
You can use this library for making any get requests easily.

### Installation

Add it to your build.gradle with:
```gradle
allprojects {
    repositories {
        maven { url "https://jitpack.io" }
    }
}
```
and:

```gradle
dependencies {
    implementation 'com.github.monusk111:NetworkCall:1.0.0'
}
```
## Adding the maven plugin
#### Step 1. Add the JitPack repository to your build file

    <repositories>
		<repository>
		    <id>jitpack.io</id>
		    <url>https://jitpack.io</url>
		</repository>
	</repositories>
	
#### Step 2. Add the dependency
    <dependency>
	    <groupId>com.github.monusk111</groupId>
	    <artifactId>NetworkCall</artifactId>
	    <version>Tag</version>
	</dependency>
    
# Usage

#### Add Internet Permission in Manifest

    <uses-permission android:name="android.permission.INTERNET"/>

#### Make a network call
    iOnDataFetched onDataFetched;
    
    TaskRunner runner = new TaskRunner();
    onDataFetched = new iOnDataFetched() {
            @Override
            public void showProgressBar() {
                //progressBar.setVisibility(View.VISIBLE);
            }

            @Override
            public void hideProgressBar() {
                //progressBar.setVisibility(View.GONE);
            }

            @Override
            public void setDataInPageWithResult(Object result) {
                if (result != null) {
                    String jsonData = result.toString();
                    processData(jsonData);
                }
            }
        };
        
#### Process Data 
    public static String TAG = "NetworkTask";
    
    private void processData(String jsonData) {
        Log.d(TAG,jsonData);
    }
    
<a href="https://www.buymeacoffee.com/monusk" target="_blank"><img src="https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png" alt="Buy Me A Coffee" style="height: 41px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;" ></a>
