---
description: >-
  Add documents such as .zip, .xls, .csv, .ppt, .docx, etc. for learners to
  download directly from the platform.
---

# Downloadable Document Button

Enable learners to download documents using a '_**Download Button**_'.&#x20;

Download buttons appear as follows in the learner view of your course:&#x20;

![](<../.gitbook/assets/Screen Shot 2021-05-27 at 12.03.36.png>)

To add download buttons to your course, please follow the steps below:&#x20;

1\) Open the Unit page where you wish to add your document.&#x20;

2\) Select to add a new '**HTML**' component.&#x20;

![](<../.gitbook/assets/Screen Shot 2021-05-27 at 12.06.09.png>)

3\) Chose '**Raw HTML'**.&#x20;

![](<../.gitbook/assets/Screen Shot 2021-05-27 at 12.06.18.png>)

4\) Select to 'Edit' the component.&#x20;

![](<../.gitbook/assets/Screen Shot 2021-05-27 at 12.06.25.png>)

5\) Remove the template text and replace it with the following code:&#x20;

```
<a class="file-download" href="/static/examplefile.pdf">Example Download PDF</a>
```

![](<../.gitbook/assets/Screen Shot 2021-05-27 at 12.06.48.png>)

6\) In a new window, open the 'Files & Uploads' page for your course. \*Please m_ake sure it's the same course_

![](<../.gitbook/assets/Screen Shot 2021-05-27 at 12.12.51.png>)

7\) Add your document(s) here using the drag + drop module on the left of the screen. You can also use the button 'Browse my computer'.&#x20;

{% hint style="danger" %}
Note, that the maximum file size is 50 mb.&#x20;
{% endhint %}

![](<../.gitbook/assets/Screen Shot 2021-05-27 at 12.14.22.png>)

8\) Remaining on the Files + Uploads page select 'Studio' to copy the Studio URL for the desired document.&#x20;

![](<../.gitbook/assets/Screen Shot 2021-05-27 at 12.16.09.png>)

9\) Back on the **Unit** page in the **Raw HTML** component, replace the `href="URL"`  with the Studio URL you copied in the previous step. This is the link for learners to download the document. &#x20;

![](<../.gitbook/assets/Screen Shot 2021-05-27 at 12.17.50.png>)

10\) Change the text for the button by replacing "Example Download PDF" with your desired text.&#x20;

11\) Select to save the changes.&#x20;
