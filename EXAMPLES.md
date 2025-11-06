# 🌎 Real World Examples

## Github Actions

- Use Github Actions which uses a simple script to automatically deploy my Laravel and React apps to a web server.

## Custom Actions

- An app that contains a status change action. The action defines an array with allowed status transitions. When called, it determines if the new status is a valid status change according to the current status and if not throws an exception.

## Scheduled Jobs

- An demo app that contains a demo user that is publicly accessible by many different users which utilizes a scheduled job to wipe out all data and re-seed the demo data every night at midnight. Used on my personal website.
- A scheduled job that takes newly hired users from an ATS system and pulls them into a separate HR application for onboarding.

## Observers

- An app that contains an observer that watches for CREATE to occur on a model, and when it does it sends out an email to the user it was created for that a new record was created for them.

## Roles & Permissions

- An app that has different user types which have their own access restrictions to certain parts of the system. I prefer a permissions-based access over role-based because you can more easily get fined tuned access levels rather than having a ton of custom roles. Permissions-based gives you specificity and customization options per user. Role-based access levels is only good for really simple apps. Used `spatie/laravel-permission`

## Multi-Tenancy

- An app that will be used my multiple clients, each having their own subdomain and their own private database. Used `archtechx/tenancy`

## Debugging

- Used Laravel Debug Bar
- Used Laravel Telescope

## Traits

- An app that used various statistical methods reused in several places in throughout the application. Converted to a `WithStatisticalMethods` trait that could be included in any class to reuse that functionality.
