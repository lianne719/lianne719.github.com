---
title: Reorganizing to a Medium-sized Flask Application
layout: post
categories: opw
tags: [mozilla, opw]
---
My Flask application has been growing in size, and I needed to reorganize my current module into a package. I learnt to do this from [Flask's documentation](http://flask.pocoo.org/docs/patterns/packages/). The small application that used to have this hierarchy:

    /relmandash
        /relmandash.py
        /relmandash_test.py
        /models.py
        /static --> for .css and .js files
        /templates --> for .html files
        /helper_packages

now looks like this:

    /relmandash
        /relmandash_test.py
        /runserver.py
        /relmandash
            /__init.py
            /view.py
            /models.py
            /static
            /templates
            /helper_packages
            
3 easy steps to shift from a module to a package:
1. Create another folder named after the application (relmandash in this case), and move everything that was required by *relmandash.py* (including *relmandash.py*) into this folder. 
2. Rename *relmandash.py* into *__init__.py*. 
3. Create a new file *runserver.py* and add these two lines:
    
    from relmandash import app  
    app.run(debug=True)

Simple! Notice how the test application is still located outside of the newly created folder. This does not change as *relmandash_test.py* just makes use of the *relmandash* package.

Since I was already re-organizing the application, I thought I might as well group my view functions (functions with @app.route above them) into another file called *views.py*. I already had a *models.py* file for my database schema declarations and the import works the same way. All I had to do for *views.py* was add this line to the top:

    from relmandash import app
    
And right at the **bottom** of *__init__.py*:

    import relmandash.views

The documentation does provide an explanation for using circular imports, so I will not go into detail here. I suppose I still don't see the need for blueprints yet, so meanwhile I'll savour my new and tidy package!
