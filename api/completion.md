---
description: API endpoints for getting completion data
---

# Completion

### Get all completion

{% swagger baseUrl="https://your-platform-url.com" path="/api/so2/v1/completion" method="get" summary="List all completions" %}
{% swagger-description %}
Get all course user completion for your instance
{% endswagger-description %}

{% swagger-parameter in="header" name="Access-Control-Request-Headers" type="string" required="true" %}
authorization
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Authorization" type="string" required="true" %}
Bearer \<auth\_token>
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Content-Type" type="string" required="true" %}
application/json
{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
{% code overflow="wrap" %}
```json
{"username":"johndoe",
"email":"john@example.com",
"course_id":"course-v1:MOOCit-demo-1",
"completion":"0.80"
}, 
{"username":"JaneDoe",
"email":"jane@example.com",
"course_id":"course-v1:MOOCit-demo-2",
"completion":"0.5"
}
...
```
{% endcode %}
{% endswagger-response %}
{% endswagger %}

### Get completion by course

{% swagger baseUrl="https://your-platform-url.com" path="/api/so2/v1/completion?course_id={course_id}" method="get" summary="List completion by course" %}
{% swagger-description %}
Get course user completion for a given course
{% endswagger-description %}

{% swagger-parameter in="header" name="Access-Control-Request-Headers" type="string" required="true" %}
authorization
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Authorization" type="string" required="true" %}
Bearer \<auth\_token>
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Content-Type" type="string" required="true" %}
application/json
{% endswagger-parameter %}

{% swagger-parameter in="query" name="course_id" type="string" %}
the course\_id course-v1:org+num+session
{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
{% code overflow="wrap" %}
```json
{"username":"johndoe",
"email":"john@example.com",
"course_id":"course-v1:MOOCit-demo-1",
"completion":"0.80"
}, 
{"username":"JaneDoe",
"email":"jane@example.com",
"course_id":"course-v1:MOOCit-demo-1",
"completion":"0.45"
}
...
```
{% endcode %}
{% endswagger-response %}
{% endswagger %}

### Get completion by username

{% swagger baseUrl="https://your-platform-url.com" path="/api/so2/v1/completion?username={username}" method="get" summary="List completion by username" %}
{% swagger-description %}
Get course completion for a given username
{% endswagger-description %}

{% swagger-parameter in="header" name="Access-Control-Request-Headers" type="string" required="true" %}
authorization
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Authorization" type="string" required="true" %}
Bearer \<auth\_token>
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Content-Type" type="string" required="true" %}
application/json
{% endswagger-parameter %}

{% swagger-parameter in="query" name="username" type="string" %}

{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
{% code overflow="wrap" %}
```json
{"username": "johndoe",
"email":"john@example.com",
"course_id":"course-v1:MOOCit-demo-1",
"completion":"0.80"
}, 
{"username": "johndoe",
"email":"john@example.com",
"course_id":"course-v1:MOOCit-demo-2",
"completion":"0.50"
}
...
```
{% endcode %}
{% endswagger-response %}
{% endswagger %}

