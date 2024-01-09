---
description: >-
  In this article we will cover how to add the ZOOM component to schedule and
  join meetings / webinars from within the platform
---

# ZOOM (SaaS Integration)

## About ZOOM Integration&#x20;

While MOOCit does not offer video-calling tools, you may add a ZOOM call to your course as an embedded component on a course page.

The ZOOM call appears differently for the instructor vs. the learners.&#x20;

The ZOOM component allows the instructors to schedule, manage and '**Start'** meetings directly via the ZOOM component on the platform.&#x20;

![](<../.gitbook/assets/Screen Shot 2021-06-11 at 11.46.41.png>)

Learners are only able to view and '**Join**' the scheduled calls:&#x20;

![](<../.gitbook/assets/Screen Shot 2021-06-11 at 11.45.24.png>)

Keep in mind, when learners or instructors '**Start**' or '**Join**' the call, the application will open in a new window prompting the user to open the call via the ZOOM app, or launch the meeting in their browser:

![](<../.gitbook/assets/Screen Shot 2021-06-11 at 11.45.46.png>)

{% hint style="info" %}
Today, there is no way to host the meeting within the embedded component, the learner will always be prompted to open a new window, or open the ZOOM app to access the call.&#x20;
{% endhint %}

You might be asking, well what is the point then? To give you an idea, some of our clients hosting blended learning environments,  create a page with an easy access to all of their ZOOM calls in the following manner:&#x20;

![](<../.gitbook/assets/Screen Shot 2021-06-11 at 11.59.34.png>)

Adding a section reserved for accessing ZOOM calls. And then using the ZOOM component as a method of access for all the scheduled live meetings:&#x20;

![](<../.gitbook/assets/Screen Shot 2021-06-11 at 12.00.04.png>)

Afterwards, you can complete the same manipulation for each chapter of the course.&#x20;

### Part One: Generate your ZOOM LTI Passport&#x20;

1\) Open the [Zoom marketplace](https://marketplace.zoom.us/apps/f8JUB3eeQv2lXsjKq5B2FA) and install the LTI Pro app. ([https://marketplace.zoom.us/apps/f8JUB3eeQv2lXsjKq5B2FA](https://marketplace.zoom.us/apps/f8JUB3eeQv2lXsjKq5B2FA))

![](<../.gitbook/assets/Screen Shot 2021-04-21 at 20.27.14.png>)

2\) Select "**Manage"** then select "**+ Create a new credential"**.&#x20;

![](<../.gitbook/assets/Screen Shot 2021-04-21 at 20.29.06.png>)

3\) Name the LTI credential "`MOOCit`" and select **LTI 1.1**. Then select "**Save**".&#x20;

![](<../.gitbook/assets/Screen Shot 2021-04-22 at 13.52.11.png>)

4\) You should arrive on the following page. Keep this page open and take notes of the **LTI URL** as well as the **LTI Key** and **LTI Secret** codes.

![](<../.gitbook/assets/Screen Shot 2021-06-10 at 16.47.52.png>)

5\) Scroll down the page to  '**Email Attribute Name**' and add `instructor_email`

![](<../.gitbook/assets/Screen Shot 2021-06-10 at 17.02.22.png>)

6\) Add **Approved Domains.**&#x20;

You must add approved domains for your LTI component, if you are a business or pro user, make sure to use your unique LMS URL. \* Please be careful not to include the '/' at the end of your URLs&#x20;

![](<../.gitbook/assets/Screen Shot 2021-06-10 at 17.21.54.png>)

### Add your ZOOM LTI Passport to MOOCit

6\) In a new window, open up your desired course and open **Settings** > **Advanced settings**

7\) Under '**Advanced Module List**', add `"lti_consumer"` . Select to **save** changes.&#x20;

![](<../.gitbook/assets/Screen Shot 2021-04-21 at 13.56.29.png>)

8\) Next, remaining on the **Advanced Settings** page, locate _**"**_** LTI Passports**_**"**_ .&#x20;

![](<../.gitbook/assets/Screen Shot 2021-06-10 at 16.24.28.png>)

9\) We will now fill in the **LTI Passport**. This passport consists of an `"id:key:secret"`&#x20;

Enter the id as `zoom`&#x20;

Next, copy and paste the '**key**' and '**secret**' code from LTI Pro App (step 3).&#x20;

You should end up with something like this: `[ "zoom:8PF7qF_OQ1KvDVzQr9Latw:yXI1TOrswzQ1zhYplS5I2duBhEFDSsGKaqSz" ]`

![](<../.gitbook/assets/Screen Shot 2021-04-22 at 13.57.12.png>)

10\) Select to **Save** the changes in the **advanced settings** (MOOCit).&#x20;

### Add your Zoom Component&#x20;

11\) From the **Course outline**, open or create the **Unit** where you wish to add your **Zoom** component.&#x20;

12\) Select to add an **Advanced Component** > **LTI Consumer** then select to **Edit** the component.&#x20;

![](<../.gitbook/assets/Screen Shot 2021-06-10 at 16.19.34.png>)

![](<../.gitbook/assets/Screen Shot 2021-06-10 at 16.19.56.png>)

13\)  Fill in the desired **display name**.&#x20;

14\) You can optionally fill in **LTI Application Information** - this is to add any relevant information about the component for your learners, i.e. to make sure they connect using their university email address as opposed to their personal account. )

15\) Next, in LTI ID enter `zoom`.&#x20;

![](<../.gitbook/assets/Screen Shot 2021-06-10 at 16.11.14.png>)

16\) Fill in the **LTI ID** with `zoom`&#x20;

17\) Fill in the **LTI URL** with the LTI URL found in your Zoom LTI Pro Application LTI credentials page (step 3). &#x20;

![](<../.gitbook/assets/Screen Shot 2021-04-22 at 14.05.53.png>)

18\) Under customer parameters add:

`["instructor_email=youremail@example.com"]`

19\) Select to **save** the component modifications.&#x20;

18\) Select to save changes.&#x20;
