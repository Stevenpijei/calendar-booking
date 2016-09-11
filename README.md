# React Booking Calendar

A responsive customizable React booking calendar.

## Demo

TODO

## Installation

```bash
npm install --save react-booking-calendar
```

## Usage

```js
import React from 'react';
import BookingCalendar from 'react-booking-calendar';

const bookings = [
  new Date(2016, 7, 1),
  new Date(2016, 7, 2),
  new Date(2016, 7, 3),
  new Date(2016, 7, 9),
  new Date(2016, 7, 10),
  new Date(2016, 7, 11),
  new Date(2016, 7, 12),
];

const MyBookingCalendar = () => (
  <BookingCalendar bookings={bookings} />
);
```

Result:

![Preview](https://github.com/kristijanbambir/react-booking-calendar/blob/master/preview.png?raw=true)

## Options

| Prop             | Type        | Default            | Description                                            |
| ---------------- | ----------- | ------------------ | ------------------------------------------------------ |
| `bookings`       | array[Date] | []                 | Dates that will be rendered on the calendar as booked. |
| `clickable`      | bool        | false              | Make days selectable.                                  |
| `disableHistory` | bool        | false              | Disable navigating before current month.               |
| `selected`       | Date        | today start of day | Default selected day if `clickable` is set.            |

## Styling

CSS class taxonomy:

```sass
.booking-calendar {
  .header {
    .header-content {
      .icon-previous {}
      .icon-next {}
      .month-label {}
    }
  }

  .week {
    &.names {
      .day-box .day {}
    }

    .day-box .day {
      &.different-month {}
      &.selected {}
      &.today {}
      &.booked-day:before {}
      &.booked-night:after {}
    }
  }
}
```

## Development

* Development server: `npm start`
* Continuously run tests on file changes: `npm run watch-test`
* Run tests: `npm test`
* Build: `npm run build`

## TODOS

- [ ] Add tests
