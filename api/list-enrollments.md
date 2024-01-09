---
description: API endpoints for getting or creating enrollments
---

# Enrollments

### Get all enrollments

{% swagger baseUrl="https://your-platform-url.com" path="/api/so2/v1/enrollments" method="get" summary="List all enrollments" %}
{% swagger-description %}
Get all course enrollments for your instance
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
"is_active":true,
"mode":"audit",
"created":"2021-03-09 20:15"
}, 
{"username":"JaneDoe",
"email":"jane@example.com",
"course_id":"course-v1:MOOCit-demo-2",
"is_active":true,
"mode":"audit",
"created":"2022-03-09 14:52"
}
...
```
{% endcode %}
{% endswagger-response %}
{% endswagger %}

### Get enrollments by course

{% swagger baseUrl="https://your-platform-url.com" path="/api/so2/v1/enrollments?course_id={course_id}" method="get" summary="List enrollments by course" %}
{% swagger-description %}
Get course enrollments for a given course
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
"is_active":true,
"mode":"audit",
"created":"2021-03-09 20:15"
}, 
{"username":"JaneDoe",
"email":"jane@example.com",
"course_id":"course-v1:MOOCit-demo-1",
"is_active":true,
"mode":"audit",
"created":"2022-03-09 14:52"
}
...
```
{% endcode %}
{% endswagger-response %}
{% endswagger %}

### Get enrollments by username

{% swagger baseUrl="https://your-platform-url.com" path="/api/so2/v1/enrollments?username={username}" method="get" summary="List enrollments by username" %}
{% swagger-description %}
Get course enrollments for a given username
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
"is_active":true,
"mode":"audit",
"created":"2021-03-09 20:15"
}, 
{"username": "johndoe",
"email":"john@example.com",
"course_id":"course-v1:MOOCit-demo-2",
"is_active":true,
"mode":"audit",
"created":"2022-03-09 14:52"
}
...
```
{% endcode %}
{% endswagger-response %}
{% endswagger %}

### Get enrollments by days

{% swagger baseUrl="https://your-platform-url.com" path="/api/so2/v1/enrollments?days={days}" method="get" summary="List enrollments by period" %}
{% swagger-description %}
Get course enrollments for the last past days&#x20;
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

{% swagger-parameter in="query" name="days" type="integer" %}

{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
{% code overflow="wrap" %}
```json
{"username": "johndoe",
"email":"john@example.com",
"course_id":"course-v1:MOOCit-demo-1",
"is_active":true,
"mode":"audit",
"created":"2021-03-09 20:15"
}, 
{"username": "johndoe",
"email":"john@example.com",
"course_id":"course-v1:MOOCit-demo-2",
"is_active":true,
"mode":"audit",
"created":"2022-03-09 14:52"
}
...
```
{% endcode %}
{% endswagger-response %}
{% endswagger %}

### Bulk enroll or unenroll users

{% swagger baseUrl="https://your-platform-url.com" path="/api/bulk_enroll/v1/bulk_enroll/" method="post" summary="Bulk enroll" %}
{% swagger-description %}
This endpoint allows you enroll or unenroll users to one or several courses.\
Permissions needed : Be a course admin for the courses you want to enroll users to.
{% endswagger-description %}

{% swagger-parameter in="header" name="Access-Control-Request-Headers" type="string" %}

{% endswagger-parameter %}

{% swagger-parameter in="header" name="Authorization" type="string" %}
Bearer \<auth\_token>
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Content-Type" type="string" %}
application/json
{% endswagger-parameter %}

{% swagger-parameter in="body" name="auto_enroll" type="Boolean" required="true" %}
true
{% endswagger-parameter %}

{% swagger-parameter in="body" name="email_students" required="true" type="Boolean" %}
true or false, set if you want to send email to notify users for enrollments
{% endswagger-parameter %}

{% swagger-parameter in="body" name="action" required="true" %}
enroll or unenroll
{% endswagger-parameter %}

{% swagger-parameter in="body" name="courses" required="true" %}
course\_id separated with comma
{% endswagger-parameter %}

{% swagger-parameter in="body" name="cohorts" required="true" %}
cohorts name separated with comma
{% endswagger-parameter %}

{% swagger-parameter in="body" name="identifiers" required="true" %}
user email separated with comma
{% endswagger-parameter %}

{% swagger-response status="200" description="Enrollments or unenrollments successful" %}
```json
{
    "action": "enroll",
    "courses": {
        "course-v1:edX+DemoX+Demo_Course": {
            "action": "enroll",
            "results": [
                {
                    "identifier": "test-email@example.com",
                    "after": {
                        "enrollment": false,
                        "allowed": false,
                        "user": true,
                        "auto_enroll": true
                    },
                    "before": {
                        "enrollment": true,
                        "allowed": false,
                        "user": true,
                        "auto_enroll": true
                    }
                }
            ],
            "auto_enroll": true
        }
    },
    "email_students": true,
    "auto_enroll": true
}
```
{% endswagger-response %}

{% swagger-response status="404" description="Not found" %}
```
```
{% endswagger-response %}
{% endswagger %}



##
