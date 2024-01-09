---
description: >-
  By default, MOOCit is integrated with YouTube. To add a Vimeo video, you must
  use an HTML component.
---

# Video - Vimeo

### Integrate a video from Vimeo&#x20;

Go to the URL of the video in Vimeo and copy the ID of the video.&#x20;

![Copy the video ID](<../.gitbook/assets/image (40).png>)

1. In Studio, in the desired **Course** > **Course Unit** add the component _**HTML > Raw HTML**_&#x20;
2. Copy and paste the code below and replace the ID with the ID number in the URL of your video. ("https://player.vimeo.com/video/**367969182**")

```markup
<div class="embed-container">
    <iframe src="https://player.vimeo.com/video/367969182" frameborder="0" webkitallowfullscreen="" mozallowfullscreen="" allowfullscreen="">
    </iframe>
</div>
```

The id # of your video must follow the `/video/` in the source`src` URL of the iframe.

{% hint style="info" %}
The "embed-container" class in which the iframe is used makes the video responsive. :wink:&#x20;
{% endhint %}

The Vimeo video is displayed in the unit responsively.

### Making Vimeo Videos Private&#x20;

{% hint style="warning" %}
Note: In order to make your videos private, you must have a paid Vimeo account. Pricing depends on the amount of storage you require, access their pricing page [here](https://vimeo.com/upgrade).
{% endhint %}

Open your video in Vimeo and select to modify the privacy settings:&#x20;

![](<../.gitbook/assets/Screen Shot 2021-06-16 at 09.19.52.png>)

Chose the option **Hide from Vimeo**.&#x20;

![](<../.gitbook/assets/Screen Shot 2021-06-16 at 09.23.28 (1).png>)

Under Embed, select 'Specific Domains'.&#x20;

![](<../.gitbook/assets/Screen Shot 2021-06-16 at 09.24.20.png>)

{% hint style="warning" %}
When you add your domains, make sure that you add your unique LMS url.
{% endhint %}

### Adding Subtitles to your Vimeo Videos &#x20;

Vimeos' [_Automatic Closed Captions_](https://help.vimeo.com/hc/en-us/articles/224968828-Captions-and-subtitles) tool is only available to their Enterprise members. If you are not on this plan, you can still add Subtitles / Captions to your video by uploading an SRT file.&#x20;

From your Video's Advanced Settings page, locate '**Distribution**' > '**Subtitles**'. Upload your SRT file by selecting the `+` (New File)  and then activate it using the blue switch located beside the SRT file name.

![](<../.gitbook/assets/Screen Shot 2021-06-16 at 09.50.37.png>)

{% hint style="success" %}
If you are looking for a free and easy way to generate subtitles for your video, we recommend using YouTube. You can upload your video (in private mode), generate your subtitles automatically, download the SRT file, and upload it to your Vimeo video. For adding subtitles to your YouTube video, please follow their tutorial here: [https://support.google.com/youtube/answer/2734796?hl=en](https://support.google.com/youtube/answer/2734796?hl=en)
{% endhint %}
