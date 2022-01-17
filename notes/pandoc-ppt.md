# Syllabus, schedule, and lecture note documents; they can be converted:

Format   | Function        | Technical Considerations
---------|-----------------|-------------------------------------------------------------------------------
Word/PDF | Writing program | Headings should match between syllabus and schedule for easy export 
HTML     | Website         | Heading level two for sections
PPTX     | Class           | Documents should be easy to splice and rework -- may need temp folder for this

To facilitate easy transfer to .pptx with Pandoc:

* The "slide level" is defined as the first header level with subsequent text
* To create a title slide, a higher-level header must be deployed

Therefore, it is in your best interest to format everything at header level two. Rather than running `pandoc --shift-heading-by` to convert to level two, just start there. A sample document follows, bring with yaml metadata. To make PowerPoint, run:

```
pandoc -i -so point.pptx file.md
```

The `-i` flag ensures that bulleted lists will appear recursively.

---
title: Title Here

---

## Heading One Here

Some contents.

::: notes

Speaker notes can be safely stowed here

:::

# Title slide

## new slide with this heading

Some content.
