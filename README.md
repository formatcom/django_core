# DJANGO CORE 2.1.2

## START SERVER
- [core.wsgi.application](core/wsgi.py)
- [get_wsgi_application](https://github.com/django/django/blob/38e2fdadfd9952e751deed662edf4c496d238f28/django/core/wsgi.py#L5)
~~~
The public interface to Django's WSGI support. Return a WSGI callable.
Avoids making django.core.handlers.WSGIHandler a public API, in case the
internal WSGI implementation changes or moves in the future.
~~~
- [WSGIHandler __init__](https://github.com/django/django/blob/38e2fdadfd9952e751deed662edf4c496d238f28/django/core/handlers/wsgi.py#L134)
- [load_middleware](https://github.com/django/django/blob/38e2fdadfd9952e751deed662edf4c496d238f28/django/core/handlers/base.py#L22)
~~~
Populate middleware lists from settings.MIDDLEWARE.
Must be called after the environment is fixed (see __call__ in subclasses).
~~~

~~~
# SET VARS
https://github.com/django/django/blob/38e2fdadfd9952e751deed662edf4c496d238f28/django/core/handlers/base.py#L28
_view_middleware = []
_template_response_middleware = []
_exception_middleware = []

https://github.com/django/django/blob/38e2fdadfd9952e751deed662edf4c496d238f28/django/core/handlers/base.py#L32
_middleware_chain = _get_response
~~~

## REQUEST SERVER
- [WSGIHandler __call__](https://github.com/django/django/blob/38e2fdadfd9952e751deed662edf4c496d238f28/django/core/handlers/wsgi.py#L138)
- [WSGIRequest](https://github.com/django/django/blob/38e2fdadfd9952e751deed662edf4c496d238f28/django/core/handlers/wsgi.py#L66)
- [get_response](https://github.com/django/django/blob/38e2fdadfd9952e751deed662edf4c496d238f28/django/core/handlers/base.py#L73)
~~~
Return an HttpResponse object for the given HttpRequest.
~~~
- [_get_response](https://github.com/django/django/blob/38e2fdadfd9952e751deed662edf4c496d238f28/django/core/handlers/base.py#L96)
~~~
Resolve and call the view, then apply view, exception, and
template_response middleware. This method is everything that happens
inside the request/response middleware.
~~~

