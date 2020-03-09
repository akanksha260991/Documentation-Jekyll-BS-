# Capture screenshots
#### Capture the screenshots of your tests to help debug better

XCode allows you to capture the screenshots for better debugging of your app. Screenshots allow the visual inspection of test executions across devices.
If you want to save the screenshots(captured by XCode) of your tests on BrowserStack, use `debugscreenshots` while executing the test:

| Param               	| Description                                                            	|
|----------------------	|------------------------------------------------------------------------	|
| debugscreenshots    	| Set this parameter to true to save the screenshots automatically captured by XCode. Screenshots can be rendered by accessing the rawlogs using the XCUITest sessions API 	|

Example:
```
curl -u "USERNAME:ACCESS_KEY" \
-X POST "https://api-cloud.browserstack.com/app-automate/xcuitest/build" \
-d '{"debugscreenshots" : true, "devices": ["iPhone 8 Plus-11"], "app": "bs://f7c874f21852ba57957a3fdc33f47514288c4ba4", "testSuite": "bs://e994db8333e32a5863938666c3c3491e778352ff"}' \
-H "Content-Type: application/json" 
```

>Note: See the [XCUIScreenshot](https://developer.apple.com/documentation/xctest/xcuiscreenshot)for details on how to capture your screenshots.