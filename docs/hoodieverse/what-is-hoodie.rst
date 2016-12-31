What is Hoodie?
===============

.. toctree::
   :maxdepth: 1
   :hidden:

   welcome-to-hoodie
   hoodie-concepts
   how-hoodie-works
   requirements
   glossary

Hoodie is backend for web applications with a JavaScript API for your frontend.
If you love building apps with HTML, CSS and JavaScript or a frontend framework,
but *dread* backend work, Hoodie is for you.

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
      })
    })

That’s how simple signing up a new user is, for example. But anyway:

**Hoodie is a frontend abstraction of a generic backend web service**.
As such, it is agnostic to your choice of frontend application
framework. For example, you can use jQuery for your web app and Hoodie
for your connection to the backend, instead of raw jQuery.ajax. You
could also use React with Hoodie as a data store, or any other
frontend framework or library, really.

Open Source
-----------

Hoodie is an Open Source project, so we don’t own it, can’t sell it, and
it won’t suddenly vanish because we got aquired. The source code for
Hoodie is available on GitHub under the Apache License 2.0.

How to proceed
--------------

You :doc:`could read up on some of the ideological concepts behind Hoodie <hoodie-concepts>`,
such as noBackend and Offline First. These explain why Hoodie exists and
why it looks and works the way it does.

If you’re more interested in the technical details of Hoodie, check out
:doc:`How Hoodie Works <how-hoodie-works>`. Learn how Hoodie handles data storage, does
syncing, and where the offline support comes from.

Eager to build stuff? Skip ahead to the :doc:`installation guide </start/index>`!
