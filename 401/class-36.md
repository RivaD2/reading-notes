# Application State with Redux

**Questions for review**

1. **What are the advantages of storing tokens in “Cookies” vs “Local Storage”?**

[codeburst.io](https://codeburst.io/localstorage-vs-cookies-all-you-need-to-know-about-storing-jwt-tokens-securely-in-the-front-end-70dc0a9b3ad3) says, "The cookie is not accessible via JavaScript; hence, it is not as vulnerable to XSS attacks aslocalStorage..."
So, this means that if you are using httpOnly and secure cookies, the cookies cannot be accessed using JavaScript. This means that even if an attacker uses JS on your site, they can't read an access token from the cookie.

[meduium.com](https://supertokens.io/blog/cookies-vs-localstorage-for-sessions-everything-you-need-to-know) says that cookies are automatically saved, sent and removed by the browser which means that the frontend dev doesn't have to worry about implementation and this also mitigates any risks.

   
1. **Explain 3rd party cookies**

Third-party cookies are cookies that are set by a website other than the one you are currently on. Third party cookies are tracked by other websites other than the one we are currently using and they are most utilized by advertisers, social media platforms and marketers.

It seems like third party cookies are EVERYWHERE! I looked at some products from a magazine called *Coveteur* today, then later I went on Instagram. Guess what, the same products I was looking up earlier on a separate site popped up on Instagram.

If you're like me and so many others out there, you probably have multiple tabs open at any given time. What I didn't realize is that a browser window with multiple tabs open counts a *single session*.  As I move across tabs, I am  relaying information about my visit history to other websites and parties. Basically I am leaving a trail of breadcrumbs of my past explorations and interests.
   
1. **How do pixel tags work?**
   
[taginspector.com](https://taginspector.com/articles/marketing-tags-and-pixels-form-and-function/) says, "A tag (or often called pixel) is a short snippet of Javascript (code) that does something on your website. In the context of marketing/advertising tags and pixels, they are often collecting some information about the visitor to a website and their behavior on the site. This is then sent back to the respective marketing/advertising platform to be processed and reported." Read on to find out **HOW** they work:

1. A user pulls up a web page, thus initiating page load.
   
2. The browser “reads” the source code of the page, embedded in the source code are the various javascript tags (like the script that you see above).

3. When the browser “reads” the part of the page where the Javascript tag/pixel is, it executes (or “fires”)
   
4. When a tag is fired, it’s given function is executed
   - For most tags, this means that tracking information is sent. The tag will capture information from the user (possible data such as user ID, the source that the user came from, location of the user, etc.), information from the page (if it’s an ecommerce site this would be information like the products being viewed, information about each product like SKU, price, color, etc. or for a content site would be information such as article title, author, etc.), and information from the URL (here is where the campaign information comes in, if using Adobe Analytics it may be the CID value or in Google Analytics it may be utm parameters).

5. The data grabbed by the tag is then sent to a third party place where it is recorded and processed, leading to the pretty analytics reports and web analytics!
  - For many tags, the request being sent will be structured as follows: `www.thirdpartydomain.com/?a=userinfo1&b=pageinfo2&c=campaigninfo3.` The first section `(thirdpartydomain.com)` shows us where the data is going and the section at the end is the data being collected in the query string. In a future section, we will discuss how to see all of this and troubleshoot tracking.

**New Vocabulary to learn:**

1. **cookies:** An HTTP cookie is a small piece of data stored on a user's computer by the web browser while browsing a website. Cookies help websites to remember stateful information or to record browsing activity
2. **authorization:** Well every time the client makes a request for a page that requires authorization, like logging in to a site for example,  the server obtains the access token from the cookie. If the token matches the one associated with the user, access is granted.
3. **access control:** Access controls authenticate and authorize individuals to access the information they are allowed to see and use. **Basically it asks the question, "Are you who you say you are and do you have the appropriate access?"**
4. **conditional rendering:** Basically it is our ability to render different UI markup based on certain conditions. Using React, it is a way to render different elements or components based on a condition.
