django_staticimport [![Build Status](https://travis-ci.org/leoxnidas/django_staticimport.svg?branch=master)](https://travis-ci.org/leoxnidas/django_staticimport)
-------------------

Add static files never was so easy. This library allows you to include css, js and images files (static files) on a template faster than the old way.


Install
-------

pip install django-staticimport


Usage.
------

####Add the app to settings.

```python

INSTALLED_APPS = [
		.
		.
		.

    'static_import',
]

```

####Then..

```html
<!DOCTYPE html>
{% load staticimport %}
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Hi</title>
	<!-- including css files -->
	{% import 'main.css' %}
	{% import 'something.css' %}
	
	<!-- including js files with custom attributes -->
	{% import 'main.js' custom='async' %}
</head>
<body>
	<!-- including images -->
	{% import 'image.jpg' css='image' id='image' custom='width="100px" height="100px" data-city="picture"' %}
	<h1>hello world</h1>
</body>
</html>
```


LICENSE
-------

Copyright (c) Leonardo Esparis and individual contributors.
All rights reserved.

Redistribution and use in source and binary forms, with or without modification,
are permitted provided that the following conditions are met:

    1. Redistributions of source code must retain the above copyright notice, 
       this list of conditions and the following disclaimer.
    
    2. Redistributions in binary form must reproduce the above copyright 
       notice, this list of conditions and the following disclaimer in the
       documentation and/or other materials provided with the distribution.

    3. Neither the name of Django nor the names of its contributors may be used
       to endorse or promote products derived from this software without
       specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND
ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED
WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT OWNER OR CONTRIBUTORS BE LIABLE FOR
ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES
(INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES;
LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON
ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT
(INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS
SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.