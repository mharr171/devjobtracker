# Dev Job Tracker

An open source web application for tracking job applications.

## Frontend


## Backend
- Ruby on Rails
 - API
 - Devise
 - ActiveAdmin
 - User Auth (TBD)

### Prospect
The prospect object will be used to house all the data related to a particular
job prospect.

| name | datatype | relation | requirement | description |
| --- | --- | --- | --- | --- |
| name | string | has_one | **YES** | Name of the company |
| discovery_type | boolean | has_one | **YES** | Self-found job or contacted by job |
| data_applied | datetime | has_one | NO | Date of application or null |
| keyword | string | has_many | NO | Keywords or 'tags' used to sort jobs |
| position_title | string | has_one | NO | Position title |
| salary_floor | integer | has_one | NO | Lower end of listed salary |
| salary_ceiling | integer | has_one | NO | Higher end of listed salary |
| requirement | string | has_many | NO | Requirements listed on job posting (years of experience, degree, etc.) |
| link | string | has_many | NO | Link to or related to job posting |
| question | text | has_many | NO | Questions related to the job, potential to be used while being interviewed |
| note | text | has_many | NO | Notes related to a listing or company |
| contact | object | has_many | NO | Contacts related to a prospect |

### Contact
The contact object will store data related to particular contacts.

| name | datatype | relation | requirement | description |
| --- | --- | --- | --- | --- |
| name | string | has_one | **YES** | Name of the contact |
| company_name | string | has_one | **YES** | Name of the company |
| title | string | has_one | NO | job title |
| phone_number | string | has_one | NO | Phone number |
| email | string | has_one | NO | Email |
| link | string | has_many | NO | Links connected to the contact (Github, LinkedIn, etc.) |
