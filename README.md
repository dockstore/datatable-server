# Purpose

A sandbox repo for combining data tables server-side processing and angular

# Required Endpoints

## Pagination

GET methods for retrieving info to populate datatables must have the parameters <b>draw</b> and <b>length</b> instead of <b>offset</b> and <b>limit</b>.

GET methods must also send back parameters expected by the data table: <b>data, draw, recordsTotal, and recordersFilters</b>.

## Search

When the user is typing into the search box, the frontend sends the param <b>search[value]</b>. We need endpoints for both containers and workflows tables' search. If the user enters 'bamstats', the tables should show 'dockstore-bamstats'.

## Ordering

When the user clicks on an orderable column, the frontend sends the param <b>order[<COL_NUM>][dir]</b> with either 'asc' or 'desc.'

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
