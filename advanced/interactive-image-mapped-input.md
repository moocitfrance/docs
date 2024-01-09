---
description: >-
  Add a background image, and have your learners click inside a defined area to
  select the answer.
---

# Pointing on a Picture Question

Use the question type '**Image Select**' / _also known as_ "**image mapped input problem**" or “**pointing on a picture**” to get your learners to find an answer within an image.&#x20;

![](<../.gitbook/assets/Screen Shot 2021-06-10 at 08.54.17.png>)

This exercise is fun and interactive for your learners, but can be a _little_ more complicated to set-up than the others, so fasten your seatbelt 🏎️  and grab your coffee ☕ ! Follow the instructions below closely, and don't hesitate to contact us (_support@moocit.fr_) if you need help. 😊

## Set-up Image Select Question

1. Choose the image you want to use, and make sure it is relatively large, and high quality.&#x20;
2. Add your image to **Studio** > **Content** > **Files and Uploads**&#x20;

![](<../.gitbook/assets/Screen Shot 2021-06-10 at 09.23.05.png>)

&#x20;  3\. Copy the web URL for your desired background image.&#x20;

![](<../.gitbook/assets/Screen Shot 2021-06-21 at 13.06.57.png>)

&#x20;  4\. **In a new tab**, open up the **Unit** where you want to add your question.&#x20;

![](<../.gitbook/assets/Screen Shot 2021-06-10 at 09.24.55.png>)

&#x20;  5\. Select to add a new **Problem Component** > **Advanced** > **Image Mapped Input**&#x20;

![](<../.gitbook/assets/Screen Shot 2021-06-10 at 09.25.22 (1).png>)

&#x20;  6\. The component will appear with a template already in place. Select to '**Edit**' the component.&#x20;

![](<../.gitbook/assets/Screen Shot 2021-06-10 at 09.26.45.png>)

&#x20;  7\. You will see the following code for the exercise:

```
<problem>
    
    <imageresponse>
        <p>What country is home to the Great Pyramid of Giza as well as the cities of Cairo and Memphis? Click the country on the map below.</p>
        <imageinput src="https://studio.edx.org/c4x/edX/DemoX/asset/Africa.png" width="600" height="638" rectangle="(338,98)-(412,168)" alt="Map of Africa"/>
        <solution>
            <div class="detailed-solution">
                <p>Explanation</p>
                <p>Egypt is home to not only the Pyramids, Cairo, and Memphis, but also the Sphinx and the ancient Royal Library of Alexandria.</p>
            </div>
        </solution>
    </imageresponse>
</problem>
```

&#x20;  8\. On line 4 between `<p>` and `</p>`, modify your question text.&#x20;

![](<../.gitbook/assets/Screen Shot 2021-06-21 at 13.04.02.png>)

&#x20;  9\. On line 5, replace the URL that appears after `<imageinput src="`to the URL of your image (copied in step 3). Keep the `" "` before and after the URL.&#x20;

![](<../.gitbook/assets/Screen Shot 2021-06-22 at 13.23.14 (1).png>)

&#x20;  10\. Also on line 5, you must change the width (`width="600"`) and height (`height="638"`) to that of your image. Ideally, your image width should not exceed 950 pixels.&#x20;
