This option allows to associate `SPDX annotations
<https://spdx.github.io/spdx-spec/v2.3/annotations/>`__ to a recipe,
using the values of variables in the recipe::

   ANNOTATION1 = "First annotation for recipe"
   ANNOTATION2 = "Second annotation for recipe"
   SPDX_CUSTOM_ANNOTATION_VARS = "ANNOTATION1 ANNOTATION2"

This will add a new block to the recipe ``.sdpx.json`` output::

   "annotations": [
     {
       "annotationDate": "2023-04-18T08:32:12Z",
       "annotationType": "OTHER",
       "annotator": "Tool: oe-spdx-creator - 1.0",
       "comment": "ANNOTATION1=First annotation for recipe"
     },
     {
       "annotationDate": "2023-04-18T08:32:12Z",
       "annotationType": "OTHER",
       "annotator": "Tool: oe-spdx-creator - 1.0",
       "comment": "ANNOTATION2=Second annotation for recipe"
     }
   ],
