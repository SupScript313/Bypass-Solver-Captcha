
Disclaimer:
By using this script, you acknowledge and agree that the developer is not responsible for any damages, losses, or liabilities resulting from the misuse of the script.
The developer has provided this script for informational purposes only and does not endorse or encourage any illegal or unethical activity.
The user assumes full responsibility for any consequences that may arise from the use of this script, and the developer disclaims any and all liability for such consequences.

Do not share this script online or with anyone else.
This is for personal use only.


Instructions:
1. Install Tampermonkey Addon or ViolentMonkey Addon (Recommended).
2. Create New script in the Tampermonkey  or ViolentMonkey Addon
3. Copy and Paste the contents in the file and save
4. Visit the website which has the captcha and check if the solver is working fine.


Configuration for 3 Icon Image Captcha:

This version has options to adjust the thresholds and also reload the page if the image cannot be identified.
To reload the page, please set the value RELOAD_PAGE_FOR_3_ICON to true in the code.
This will avoid incorrect solutions to some extent.

Known Issues:
If the status shows "Closest Match Found" but the icon has not been clicked, it usually means that pop-ups are blocked.
Some websites open a pop-up window after the icon is clicked.
Make sure to enable pop-ups for the website in your browser settings.

Another possible reason is the presence of a "Allow Cookies" banner or pop-over.
In this case, you must accept the cookies and reload the page for the feature to work correctly.

If the answer submitted is consecutively wrong twice, you have to delete the cookies and local storage,
then start the shortlink again.

You can also do this by pasting the following code in the browser console.

// Local Storage
  localStorage.clear();

// Delete all cookies
  document.cookie.split(";").forEach(cookie => {
      const name = cookie.split("=")[0].trim();
      document.cookie = `${name}=;expires=Thu, 01 Jan 1970 00:00:00 GMT;path=/`;
  });




Training New Images for single Icon Image:
1. The script includes a trainer which is disabled by default. To enable trainer, please set the value ENABLE_TRAINER to true in the code.
2. The training logs can be viewed in browser console.
3. The images are stored in UserScript Storage. You can view the data in Userscript Settings/Storage.
4. The stored data can be copied to other browser. 

AI based Remote Solver for single Icon Image:
1. The script includes code to enable solving on remote server. 
2. To enable remote solving, please set the value of ENABLE_REMOTE_SOLVER to true in the code.
3. Allow Pop Ups for first run else it may not work.
4. If you see Puter pop up with Sign In page, please sign up using email and password and login. Then reload the faucet website page.
5. If you have any issues relates to puter, use incognito mode in browser.


Adding new websites inside the script:
To use the solver on other websites follow the steps below.

1. Add your website name in the matcher section at the top of this script to work.
2. You may have a look at other websites added with @match at the top
3. Don't try to add global matcher if there are too many websites since it will consume more resources. Add it only when necessary
4. The script does not work in iframes by default. If you have website which is inside iframe, remove @noframes at the top.


Note:
This has been tested in chrome.


