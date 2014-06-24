sphinxcontrib-httpdomain
========================

Fork of sphinxcontrib-httpdomain (https://pypi.python.org/pypi/sphinxcontrib-httpdomain) that allows for deduplication of flask routes.


Example:
--------
```
.. autoflask:: your_flask_app:app
	:undoc-static:
	:include-empty-docstring:
	:deduplicate-routes:
```

Before:
-------
```
GET /Collections/
GET /collections/
GET /test
GET /Test
GET /
GET /Collection/(int: id)
GET /collection/(int: id)
```

After:
------
```
GET /test
GET /collection/(int: id)
GET /collections/
GET /
```


sphinxcontrib.httpdomain --- Documenting RESTful HTTP APIs
==========================================================

This contrib extension, sphinxcontrib.httpdomain, provides a Sphinx domain
for describing RESTful HTTP APIs.

You can find the documentation from the following URL:

http://pythonhosted.org/sphinxcontrib-httpdomain/

