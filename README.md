# DJANGO CORE 2.1.2

## START SERVER
- [core.wsgi.application](core/wsgi.py)
- [get_wsgi_application](https://github.com/django/django/blob/38e2fdadfd9952e751deed662edf4c496d238f28/django/core/wsgi.py#L5)
- [WSGIHandler __init__](https://github.com/django/django/blob/38e2fdadfd9952e751deed662edf4c496d238f28/django/core/handlers/wsgi.py#L134)
- [load_middleware](https://github.com/django/django/blob/38e2fdadfd9952e751deed662edf4c496d238f28/django/core/handlers/base.py#L22)

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
- [_get_response](https://github.com/django/django/blob/38e2fdadfd9952e751deed662edf4c496d238f28/django/core/handlers/base.py#L96)

