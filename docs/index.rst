Welcome to Hoodie
=================

.. toctree::
   :maxdepth: 2
   :glob:

   hoodieverse/*
   start/*
   tutorials/*
   techdocs/*
   plugins/*
   deployment/*
   community/*

What is Hoodie?
---------------

Hoodie is backend for web applications with a JavaScript API for your frontend.
If you love building apps with HTML, CSS and JavaScript or a frontend framework, but *dread* backend work, Hoodie is
for you.

Hoodie gives your frontend code superpowers by allowing you to do things
that usually only a backend can do (user accounts, emails, payments,
etc.).

All of Hoodie is accessible through a simple script include, just like
jQuery or lodash:

.. code:: html

   <script src="/hoodie/client.js"></script>
   <script type="javascript">
     var hoodie = new Hoodie();
   </script>

From that point on, things get really powerful really quickly:

.. code:: javascript

    // In your front-end code:
    hoodie.ready.then(function () {
      hoodie.account.signUp({
        username: username,
        password: password
      });
    })

That’s how simple signing up a new user is, for example. But anyway:

**Hoodie is a frontend abstraction of a generic backend web service**.
As such, it is agnostic to your choice of frontend application
framework. For example, you can use jQuery for your web app and Hoodie
for your connection to the backend, instead of raw jQuery.ajax. You
could also use Backbone with Hoodie as a data store, or any other
frontend framework, really.

Open Source
-----------

Hoodie is an Open Source project, so we don’t own it, can’t sell it, and
it won’t suddenly vanish because we got aquired. The source code for
Hoodie is available on GitHub under the Apache License 2.0.

How to proceed
--------------

You `could read up on some of the ideological concepts behind Hoodie`_,
such as noBackend and Offline First. These explain why Hoodie exists and
why it looks and works the way it does.

If you’re more interested in the technical details of Hoodie, check out
`How Hoodie Works`_. Learn how Hoodie handles data storage, does
syncing, and where the offline support comes from.

Eager to build stuff? Skip ahead to the `installation guide`_!

.. _could read up on some of the ideological concepts behind Hoodie: /camp/hoodieverse/hoodie-concepts.html
.. _How Hoodie Works: /camp/hoodieverse/how-hoodie-works.html
.. _installation guide: /camp/start/
