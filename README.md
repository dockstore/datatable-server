# Purpose

A sandbox repo for combining data tables server-side processing and angular

# Required Endpoints

Expected Returned Data Parameters: draw, recordsTotal, recordsFiltered, data, error

## Pagination

Important Sent Parameters: draw, length

The API already has offset and limit in place, simply rename them to be draw and length, respectively. The parameter draw acts as the page number, except it is starting from 0 rather than 1. The parameter length is the number of entries per page. If draw is 2, and the length is 10, the GET method should return <b>data</b> containing information from the 31st tool to the 40th tool (3 pages * 10 entries/page = 30 entries are in the pages before). The parameter <b>recordsTotal</b> indicates how many records for which pagination needs to be done.

## Search

Important Sent Parameter: search[value]

When the user is typing into the search box, the frontend sends the param <b>search[value]</b> with a call to the GET method. Ideally, the callback should only occur after the user stops typing. See an example here: [Search Using Observables]("https://blog.thoughtram.io/angular/2016/01/06/taking-advantage-of-observables-in-angular2.html").

## Ordering

Important Sent Parameter: order[COL_NUM][dir]

When the user clicks to order a column, the frontend sends the param <b>order[COL_NUM][dir]</b> with either 'asc' or 'desc' with a call to the GET method. The backend should reorder the entries and return the result.

For more information visit [Data Tables Server-Side Processing.("https://datatables.net/manual/server-side#Example-data");

# Datatable

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 1.0.0-rc.4.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive/pipe/service/class/module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `-prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).
Before running the tests make sure you are serving the app via `ng serve`.

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).
