# README - Image folder

* For your book chapter, create one folder "images-team-name" that is unique to your team and contains all images.

* Instead of relying on on line images, copy images to this local folder to ensure they stay there as the web evolves

* Double check image copy rights, and include appropriate attribution.

* Optionally crop out extra white space surrounding the image

* Use the standard markdown to include images, i.e.

    
```
    ![Optional ALT text](images-YOUR-PROJECT/image.png)
    *Your Caption Here*
```

Note that he caption is _immediately after_ the image (no new line). In this way, pandoc (for pdf and epub) as well as Jekyll can generate decent image captions.

This approach is based on a [Stack Overflow][so-captions] answer on using image captions in Jekyll (which always ignores alt attributes in its main text). This solution [also works in pandoc][pandoc-captions], which only ignores an alt text in the main text if there is a caption text immediately after the image.

If you wish you can include a figure number in your caption, but there is no automated figure numbering.

If you do _not_ want _any_ caption, my trick is to put empty comments just below the image:

    ![](...)
    <!-- -->

This comment then serves to trick pandoc into not generating an empty "Figure 3.1: " caption.


[so-captions]: http://stackoverflow.com/a/30366422/165292
[pandoc-captions]: https://groups.google.com/forum/#!topic/pandoc-discuss/j3x6Zafj9Fs
