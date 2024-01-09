# H5P

### What is H5P_?_

H5P is a free and open-source content collaboration framework based on JavaScript. H5P is an abbreviation for HTML5 Package, and aims to make it easy for everyone to create, share and reuse interactive HTML5 content.

Using H5P, you can create additional types of interactive content including quizzes, games, calculators and more, and use them in your course!&#x20;

Here's a glimpse of a few components available on H5P: \
[_(see the full list here)_ ](https://h5p.org/content-types-and-applications)

![A few examples of H5P exercises and activities](<../.gitbook/assets/Screen Shot 2020-08-27 at 13.45.15.png>)

### Adding H5P Components to Your Course

1\) Create an account on H5P ([link](https://eu-west-1.h5p.com/register))\
2\) Login to your account ([link](https://h5p.com/login/introduce))\
3\) In the header menu select _< + Add Content  >_ \
4\) Select and create the desired content type. 'Save' when you're done.&#x20;

{% hint style="info" %}
**TIP:** You can create as many H5P components as you like! There are tutorials / examples available on the H5P website in case you need help.&#x20;
{% endhint %}

5\) In the header menu select < _Manage Organization_ > \
6\) Select < _Add LMS Connection_ >\
7\) Choose 'Other' for your LMS, enter a connection name and choose the LTI v1.1 version. &#x20;

![](<../.gitbook/assets/Screen Shot 2020-08-27 at 15.57.43.png>)

\
8\) Select to 'Save', and keep the window / tab open. \
9\) In a new window / tab, open your course in MOOCit Studio\
10\) Select _Settings_ > _Advanced Settings_\
11\) Under 'Advanced Module List' add "lti\_consumer"

![](<../.gitbook/assets/Screen Shot 2020-08-27 at 16.07.56.png>)

12\) Obtain the key + secret by select 'Manage Organization' > 'Connect LMS'  in your H5P account.&#x20;

![](<../.gitbook/assets/Screen Shot 2020-08-27 at 16.33.35.png>)

\
13\) Back in Studio > Advanced Settings, locate 'LTI Passports', and add: "id:key:secret".

![](<../.gitbook/assets/Screen Shot 2020-08-27 at 16.32.36.png>)

14\) Save changes in Studio > Advanced Settings. \
15\) Open up the course unit where you wish to add the H5P component.\
16\) Under 'Add New Component' Select 'Advanced' > 'LTI Consumer'\
17\) Select to edit the component. \
18\) In your h5P account select 'Manage Content' and right click on the desired component to copy it's web URL. \


![](<../.gitbook/assets/Screen Shot 2020-08-27 at 16.49.11.png>)

19\) Back in Studio, in the LTI Consumer Component Editor, add\
LTI ID = id\
LTI URL = 'paste your URL' \
Select to save.

![](<../.gitbook/assets/Screen Shot 2020-08-27 at 16.51.10.png>)

20\) Select to 'Publish' and 'View Live'&#x20;

🥳 Congratulations! You've just configured your H5P Component!&#x20;

###
