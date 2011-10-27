Mailifier – Hide email addresses from spambots
==============================================

Mailifier allows you to display emailaddresses in webpages whilst preventing spambots from harvesting them.

Features
--------

* Malifier is fast and compact.
* Being a jQuery plugin it is easily implemented.
* It allows for easy extending and customization.

Example
-------

Original HTML:

    <span class="email">user [at] example [dot] com</span>

Javascript:

    $("span.email").emailify();

Resulting HTML:

    <span class="email"><a href="mailto:user@example.com">user@example.com</a></span>
    
View this example at [jsfiddle](http://jsfiddle.net/voormedia/r29EM/).

Requirements
------------

jQuery 1.4.4 or higher.

Instructions
------------

1. Include the plugin on your web page:

    <script src="jquery.vm.emailifier.min.js" type="text/javascript"></script>
  
2. Contain obfuscated emailadresses in an arbitrary element:

    `<span class="email">tim [at] example [dot] com</span>`
    `<span class="email">bob [at] example [dot] com</span>`
  
3. Emailify the addresses:

    `$(document).ready(function() {`
       `$("span.email").emailify();`
    `});`

Parameters
----------

The options are to be passed in an object. None are mandatory.

<table>
<tr><th>OPTION</th><th>TYPE</th><th>DEFAULT</th><th>REMARK</th></tr>
<tr><td>atSign</td><td>string</td><td>" [at] "</td><td>String that will be replaced by '@'.</td></tr>
<tr><td>dotSign</td><td>string</td><td>" [dot] "</td><td>String that will be replaced by '.'.</td></tr>
<tr><td>substitute</td><td>function(string)</td><td></td><td>The substitute html can be customized by passing in a function. It receives the deobfuscated address as a parameter and should return the substitute html.</td></tr>
</table>
                             
About Emailifier
----------------

Emailifier was developed by Roel van Dijk, Anne Fortuin, Rolf Timmermans and Thijs Brilleman.

Copyright 2011 Voormedia - [www.voormedia.com](http://www.voormedia.com)

License
-------

Emailifier is released under the MIT license.