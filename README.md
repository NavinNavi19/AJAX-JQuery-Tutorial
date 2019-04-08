# AJAX-JQuery-Tutorial

Key Takeaway from JQuery's AJAX

## Overview and Setup

- Completed Intro on the course 3 page todo app.
- I refracted the code to use Promise with then and catch instead of callback.

## AJAX GET Request

```js
$.get("/todos", data => {
  debugger;
});
```

## AJAX POST Request

```js
var values = {};
$("form").submit(e => {
  e.preventDefault();
  var formData = $("form").serialize();
  $.post("/todos", formData, data => {
    console.log(data);
  });
});
```

## PUT and DELETE Request

-EDIT

```js
var values = {};
$("form").submit(e => {
  e.preventDefault();
  let formData = $("form").serialize();
  let formAction = $("form").attr("action");
  console.log(formAction);
  $.ajax({
    url: formAction,
    data: formData,
    type: "put",
    success: function(data) {
      debugger;
    }
  });
});
```

- DELETE

```js
$("form").submit(e => {
  e.preventDefault();
  let formAction = $("form").attr("action");
  console.log(formAction);
  $.ajax({
    url: formAction,
    type: "delete",
    success: function(data) {
      debugger;
    }
  });
});
```

- Moved Create new Todo to the Home Page.
- Moved Edit Todo Form to the Home Page.
- Updated Edit Form with updated Form.
- Updated Delete Request Form with updated Form.
- Made the applicaion into a single page application.

## Microservices

- Divided my app into two seperate app as client and server side.
- 
