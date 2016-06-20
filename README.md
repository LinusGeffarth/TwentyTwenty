# TwentyTwenty
Handy &amp; Pretty Side by Side Picture Comparison

This library allows you to compare picture side by side. Here are instructions for the use of the library with iOS in Swift. All credits for the library go to <a href="http://zurb.com/playground/twentytwenty">zurb studios</a>.

## Use

1. Import the index.html file into your project (make sure to *check* 'Copy items if needed')

2. Import the two .css and all three .js files (again, check 'copy')

3. Go to **Build Phases** –> **Copy Bundle Resources**, make sure all 6 files are listed there

4. In your ViewController, to use the library with a UIWebView, paste the following code:

    `var html: NSString = ""`<br>
    `let htmlFile = NSURL(fileURLWithPath:NSBundle.mainBundle().pathForResource("index", ofType:"html")!)`<br>
    `do {`<br>
    `    html = try NSString(contentsOfURL: htmlFile, encoding: NSUTF8StringEncoding)`<br>
    `} catch {}`<br>
    `webView.loadHTMLString(html as String, baseURL: htmlFile)`<br>

5. Now, import two pictures of your choice. Go through step 3 for the pictures again.

6. Modify the following code to make it display your pictures:

    `<div class="twentytwenty-container">`<br>
      `<img src="[YOUR BEFORE PICTURE'S NAME].jpg"/>`<br>
      `<img src="[YOUR AFTER  PICTURE'S NAME].jpg"/>`<br>
    `</div>`<br>

7. You should be good to go. Now run your project!
