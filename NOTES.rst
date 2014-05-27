General Comments
================

When a new and old way of doing things exists, do not even mention
the old way to 'new' trainees.
In the munich training, most people of have not used plone for <= 1 yr,
so ancient dragons, even if they still are present but sleeping, need not be awoken in the minds of the new.


Important things learnt
=======================
 - Never log in to a public site with the Zope user, as the username 
   and password will be in the request headers (base64 encoded)

LOL moments
===========

* Trouble with grok is sometimes you ask for a banana and get a gorilla holding a banana. 

* If you have a site that has to be mainained for a number of years, and go though upgrades, be sure to invest time in investiating addons you use. If you choose an addon such as **singing and dancing**, you will cry inside for years. (!!)


Not covered / problems
======================
 - plone.app.testing
  - Use of <includeDependencies> in ZCML

 - ZopeSkel problem reared its head
 - Training uses zopeskel from Unified installer, which creates outdated stuff that trainees were asked to delete
   Mentioned that starzel use mr.bob.

   What works for me:
    - templer for projects
    - Latest zopeskel in the 2.x line (not 3.x which is for templer)

Explaining nocall:
==================

Not a 'generator' at all (as Philip said)
Better to provide an example in the python interactive interpretter such as:

>>> a = dict(a=1, b=1)
>>> keys = a.keys # nocall:a/keys
>>> keys()



Explaining BrowserView
======================
No need to explain the __init__ metthod in the browser view for newbies?
Better to just say - do not put any customizations in the __init__ method
for your browser view, do it in __call__.


Use plone.api.portal.get_tool instead of getToolByName?
=======================================================

Accessing field on brains
=========================
This should be using __getitem__ syntax instead of getattr

brain['Title']


Addons to consider/investigate
==============================
 * collective.mailchimp  (commercial) Timo Stollenburg
 * collective.quickupload (Drag & drop multiple files)
 * FTWUpgrade
 * Products.PDBDebugMode
 * plone.app.debugtoolbar

