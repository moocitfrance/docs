---
description: Add a PDF without giving learners the option to download / print the document.
---

# PDF viewer without download / print option

By default, all PDF viewers offer the option to download / print the document.

![](<../.gitbook/assets/Screen Shot 2021-05-27 at 14.01.39.png>)

&#x20;If you wish to prohibit the copying of the PDF documents (download, print, save-as), please follow the steps below.&#x20;

{% hint style="warning" %}
Note: In order to privatise our PDF documents, we will be using Google Drive. You must have a Google account to proceed with this tutorial.&#x20;
{% endhint %}

### Protect your PDF documents with the help of Google Drive

1\) Add your **PDF** to your **Google Drive** account. Select the **3 vertical dots menu** in the upper right hand corner.

![](<../.gitbook/assets/Screen Shot 2021-05-27 at 14.10.18.png>)

2\) Select '**Share**'&#x20;

![](<../.gitbook/assets/Screen Shot 2021-05-27 at 14.19.28.png>)

3\) Select the **gear icon** '_**Share with people settings**_'.&#x20;

![](<../.gitbook/assets/Screen Shot 2021-05-27 at 14.20.33.png>)

4\) Deselect the options: \
\- Editors can change permissions and share\
\- Viewers and commenters can see the option to download, print, and copy

![](<../.gitbook/assets/Screen Shot 2021-05-27 at 14.22.02.png>)

5\) Select the **Back** arrow to return to the sharing menu.&#x20;

![](<../.gitbook/assets/Screen Shot 2021-05-27 at 14.23.03.png>)

6\) Under **Get Link** select to _**Change Link**_&#x20;

![](<../.gitbook/assets/Screen Shot 2021-05-27 at 14.24.04.png>)

7\) Below the '**Get Link**' URL, select the _drown-down menu_ to chose who the document will be shared with, and select '_**Anyone with Link**_'&#x20;

![](<../.gitbook/assets/Screen Shot 2021-05-27 at 14.26.16.png>)

On the right, make sure you have selected '**Viewer**' and not '_**Commenter**_' or '_**Editor**_'. Because learners should only be able to 'view' the document, not 'comment' or 'edit'. :)&#x20;

![](<../.gitbook/assets/Screen Shot 2021-05-27 at 14.27.48.png>)

8\) Select '_**Copy Link**_' and then select '_**Done**_'.&#x20;

{% hint style="warning" %}
Keep this window open and open studio in a new tab so that you may easily re-access the Google URL if necessary.
{% endhint %}

![](<../.gitbook/assets/Screen Shot 2021-05-27 at 14.30.58.png>)

9\) Open the **Course** > **Unit** where you want to add the PDF. Select to add an **HTML** component > **Raw HTML**.&#x20;

![](<../.gitbook/assets/Screen Shot 2021-05-27 at 14.35.15 (1).png>)

![](<../.gitbook/assets/Screen Shot 2021-05-27 at 14.35.21.png>)

10\) Select to '**Edit**' the component.&#x20;

![](<../.gitbook/assets/Screen Shot 2021-05-27 at 14.37.26.png>)

and replace the text with the following code:&#x20;

```
<iframe src="
https://drive.google.com/file/d/1hOzPHBqg-BlU716fr1vyyUD9zlJMHGu3/preview
" width="100%" height="900"></iframe>
```

![](<../.gitbook/assets/Screen Shot 2021-05-27 at 14.37.41.png>)

11\) Replace the `src=` URL with your Google Drive PDF URL (Step 8).&#x20;

![](<../.gitbook/assets/Screen Shot 2021-05-27 at 14.39.40.png>)

You can also modify the height and/or width (in pixels) of the PDF viewer.&#x20;

Select to '**Save**' the changes.&#x20;
