---
description: API endpoints for getting grade data
---

# Grades

### Get all grades

{% swagger baseUrl="https://your-platform-url.com" path="/api/so2/v1/grades" method="get" summary="List all grades" %}
{% swagger-description %}
Get all course user grades for your instance
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
"display_name": "MOOCit demonstration Course #1",
"percent_grade":"0.80",
"letter_grade":"Pass",
"passed_timestamp":"2020-03-28 23:21:24.354019"
"last_date":"2020-11-26"
}, 
{"username":"JaneDoe",
"email":"jane@example.com",
"course_id":"course-v1:MOOCit-demo-2",
"display_name": "MOOCit demonstration Course #2",
"percent_grade":"0.20",
"letter_grade":"",
"passed_timestamp":null
"last_date":"2020-11-26"
}
...
```
{% endcode %}
{% endswagger-response %}
{% endswagger %}

### Get grades by course

{% swagger baseUrl="https://your-platform-url.com" path="/api/so2/v1/grades?course_id={course_id}" method="get" summary="List grades by course" %}
{% swagger-description %}
Get course user grades for a given course
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
"display_name": "MOOCit demonstration Course #1",
"percent_grade":"0.80",
"letter_grade":"Pass",
"passed_timestamp":"2020-03-28 23:21:24.354019"
"last_date":"2020-11-26"
}, 
{"username":"JaneDoe",
"email":"jane@example.com",
"course_id":"course-v1:MOOCit-demo-2",
"display_name": "MOOCit demonstration Course #1",
"percent_grade":"0.20",
"letter_grade":"",
"passed_timestamp":null
"last_date":"2020-11-26"
}
...
```
{% endcode %}
{% endswagger-response %}
{% endswagger %}

### Get grades by username

{% swagger baseUrl="https://your-platform-url.com" path="/api/so2/v1/grades?username={username}" method="get" summary="List grades by username" %}
{% swagger-description %}
Get course grades for a given username
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
{"username":"johndoe",
"email":"john@example.com",
"course_id":"course-v1:MOOCit-demo-1",
"display_name": "MOOCit demonstration Course #1",
"percent_grade":"0.80",
"letter_grade":"Pass",
"passed_timestamp":"2020-03-28 23:21:24.354019"
"last_date":"2020-11-26"
}, 
{"username":"johndoe",
"email":"john@example.com",
"course_id":"course-v1:MOOCit-demo-1",
"display_name": "MOOCit demonstration Course #1",
"percent_grade":"0.20",
"letter_grade":"",
"passed_timestamp":null
"last_date":"2020-11-26"
}
...
```
{% endcode %}
{% endswagger-response %}
{% endswagger %}

