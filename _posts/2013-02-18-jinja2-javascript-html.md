---
title: Jinja2 templates, Javascript and HTML
layout: post
categories: opw
tags: [mozilla, opw]
---
I've been using Flask to build the release dashboard, and so far the building and configuration have been the definition of smooth sailing. However, it took me two weeks to realize the templates for HTML output do not make use of something the developers of Flask built themselves, but a syntax named Jinja2! *So much for skim-reading the tutorials.* Take this simple code,

    { % for elem in array % }
        <p>{ { elem } }</p>
    { % endfor % }
    
Turns out, if i wanted to check if *array* was empty before looping, I could do

    { % if array % }
        # loop and print
    { % else % }
        # print something else
    { % endif % }
    
I found that out from Django's docs and thought that I was using the Django template syntax all along! P.S.: I tried *count(array), len(array), array|length, array.size* and the list goes on...

Similar to mixing HTML in between Jinja2 syntax, a template doesn't need to have Javascript and Jinja2 as separate blocks of code. Instead of pure Javascript:

    <script type=text/javascript>
        function print_table(type) {
            $.getJSON($SCRIPT_ROOT + '/' + type, function(data) {
                if (data.result.length > 0) {
                    var table = 
                        ['<thead><tr><th>ID</th></tr></thead>'];
                    $.each(data.result, function(index, bug) {
                        table.push('<tr><td>' + bug.id + '</td></tr>');
                        }
                    });
                    $('<table/>', {
                        html: table.join('')
                    }).appendTo('body');
                } 
            });
        }
    </script>
    
one can do 

    { % if beta % }
        <table>
            <thead><tr><th>ID</th></tr></thead>
            <tbody>
            { % for bug in beta % }
                <tr><td>{{bug.id}} </td></tr>
            { % endfor % }
            </tbody>
        </table>
    { % endif % }
    
for the same output, though the former uses Javascript to obtain the list in JSON after the page has loaded.
