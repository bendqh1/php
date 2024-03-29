# Images copied from a website are pasted but images copied from an operating system are not pasted

I have the problem that after upgrading Drupal 9 to Drupal 10 with CKEditor 5, I can no longer paste clipboard-copied images into CKEditor unless they are copied from a a webpage.

## Use case

I have tried to copy-paste the following image not from a webpage, but from Windows 11 [Photos][1] application, but failed.

[![enter image description here][1]][1]

### CKEditor 5 image uploading tool screenshots

Here are screenshots of my CKEditor 5 image uploading tool:

[![enter image description here][2]][2]
<br>
[![enter image description here][3]][3]

## Interim note

This problem happens only in a Drupal that was upgraded from 9 to 10, but in another Drupal that was installed as 10 from the start, it doesn't happen and I can paste images copied either from a webpage or from a local operating system.

# Solution

The problem was caused in the particular website I have mentioned due to not having the CKEditor option to upload images **on**, for the particular text format I work with (Full HTML).

To solve the problem I went to `/admin/config/content/formats/manage/full_html`, where I went to **CKEditor 5 plugin settings**, where I chose the **Image** settings, where I checkmarked **"Enable image uploads"** and then saved the new settings.

<hr>

## Before:

[![enter image description here][4]][4]

## After:

[![enter image description here][5]][5]

<hr>

After doing that, I could copy-paste images from the operating system directly (i.e not from a webpage) without any problem.


  [1]: https://i.stack.imgur.com/vTbod.png
  [2]: https://i.stack.imgur.com/sE70H.png
  [3]: https://i.stack.imgur.com/na3YG.png
  [4]: https://i.stack.imgur.com/6Zv1y.png
  [5]: https://i.stack.imgur.com/ML8n0.png
