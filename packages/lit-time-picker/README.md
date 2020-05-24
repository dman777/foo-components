## lit-time-picker

Web component time picker written in lit element. This was originally developed as a proof of concept, but due to the popularity of it I will continue development of it.

![Image of lit-time-picker](https://imgur.com/a/hNJPt5N)

###### To do: Add custom styling properties.

##### Usage

```html
<head>
  <script type="module" src="/src/lit-time-picker.js"></script>
</head>
<body style="display: flex; justify-content: center; margin-top: 200px;">
  <lit-time-picker on-time-changed="_doSomethingWithNewTime" time-date-stamp="2020-05-04T04:33:21.511Z"></lit-time-picker>
</body>
  <script>
    const el = document.querySelector('lit-time-picker');
    const _doSomethingWithNewTime = (e) => {
      console.log(e);
    }
    el.addEventListener('time-changed', _doSomethingWithNewTime);
  </script>
```

###### Note: `<lit-time-picker on-time-changed="_doSomethingWithNewTime"></lit-time-picker>` will default to current time

##### properties
`time-date-stamp` set the time date of the component. Must be in ISO format(don't worry, it will convert to local meridiem time).

##### events
`time-changed` return object containing ISO format and also moment object for any time mutation.

###### event object:

```javascript
detail:
  momentObj: Moment {_isAMomentObject: true, _i: "2020-05-03T06:33:21.511Z", _f: "YYYY-MM-DDTHH:mm:ss.SSSSZ", _tzm: 0, _isUTC: false, …}
  timeStampISO: "2020-05-03T06:33:21.511Z"
```


