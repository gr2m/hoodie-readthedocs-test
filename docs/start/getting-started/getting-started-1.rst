Getting Started with Hoodie - Part 1
====================================

This is the first part of Getting Started with Hoodie, which describes
the first steps after you’ve successfully `installed Hoodie and its
prerequisites`_. In this guide you’ll learn how to create a demo Hoodie
app, learn about the basic structure of a Hoodie project and its
folders, the endpoints and app URLs and how to include and use the
Hoodie library in your project.

Topics Covered in this guide
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

1. Creating a new app
2. Structure of a Hoodie Project
3. Including the Script
4. The global window.hoodie Object

If you experience any problems at any step of this doc, please check our
FAQ or get in touch with us on IRC or Slack.

1. Creating a new Hoodie app
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

First you need to create a new folder, let’s call it **testapp**

.. code:: bash

    $ mkdir testapp

Change into the ``testapp`` directory.

.. code:: bash

    $ cd testapp

Now we need to create a **package.json** file. For that we can use
`npm`_ which comes with Node by default. It will ask you a few
questions, you can simply press enter to leave the default values.

.. code:: bash

    $ npm init

If you are interested, here are docs on the `npm init`_ command.

Now we can install **hoodie** using npm

.. code:: bash

    $ npm install hoodie --save

If you are curious what happens in the background, here are docs for the
`npm install`_ command.

Now you need to edit the **package.json** file. We need to set the
**“start”** script to **“hoodie”**. The result should look something
like this

.. code:: json

    {
      "name": "funky",
      "version": "1.0.0",
      "description": "",
      "main": "index.js",
      "scripts": {
        "start": "hoodie",
        "test": "echo \"Error: no test specified\" && exit 1"
      },
      "keywords": [],
      "author": "",
      "license": "ISC"
    }

Now you can start the app

.. code:: bash

    $ npm start

Great, your app started up and is now telling you at which URL you can
access your app. By default that is http://127.0.0.1:8080

Congratulations, you just created your first Hoodie App :)

2. Structure of a Hoodie Project
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

public folder
^^^^^^^^^^^^^

When you open your app in the browser you will see Hoodie’s default page
telling you that your app has no **public/** folder. So let’s create it

.. code:: bash

    mkdir public
    touch public/index.html

Now edit the **public/index.html** file and pass in the following
content.

.. code:: html

    <!DOCTYPE html>
    <html lang="en">
      <head>
        <meta charset="utf-8">
        <title>My Hoodie App</title>
      </head>
      <body>
        <h1>My Hoodie App</h1>

        <script src="/hoodie/client.js"></script>
      </body>
    </html>

You need to stop the server now (**ctrl** + **c**) and start it again.
If you reload your app in your browser, you will now see your HTML file.

The only line interesting for us is t

.. _installed Hoodie and its prerequisites: /camp/start/
.. _npm: https://www.npmjs.com/
.. _npm init: https://docs.npmjs.com/cli/init
.. _npm install: https://docs.npmjs.com/cli/install
