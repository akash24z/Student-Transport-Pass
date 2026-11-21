# Student Transport Pass Request System

A responsive web application where students request a transport pass and an admin reviews, approves or rejects those requests. Built with plain HTML, CSS and JavaScript, with no backend or framework.

## Project details

| | |
|---|---|
| Project title | Student Transport Pass Request System |
| Team name | YOUR-TEAM-NAME |
| Course code | YOUR-COURSE-CODE |

**Team members**

| Name | Registration number |
|---|---|
| Member 1 | 00000000 |
| Member 2 | 00000000 |
| Member 3 | 00000000 |

## Problem statement

Develop a responsive web-based solution for a student transport pass request system that organizes the required information, simplifies the main workflow, supports clear user actions, and provides useful status or summary views.

## Features

**Student side**
- Pass request form with name, registration number, email, mobile, course, pickup stop, route, pass type and start date.
- Live fee calculation when the route and pass type are chosen (Quarterly gets 10% off, Semester gets 15% off).
- Input validation with clear error messages under each field, and a success message on submit.
- Duplicate protection: the same registration number cannot have two pending requests on the same route.
- Track request: search by registration number to see the request status (Submitted, Under review, Approved or Rejected), validity dates for approved passes, and the reason for rejected ones.

**Admin panel**
- Sign in with a username and password.
- Dashboard with total, pending, approved and rejected counts, fees from approved passes, and a requests-by-route chart.
- Search by name, registration number, ID or email.
- Filter by status, route and pass type.
- Approve, reject (with a reason), edit and delete requests.
- Export all requests as a CSV file.

**General**
- Responsive layout for mobile, tablet and desktop.
- Animations that respect the "reduce motion" setting of the device.

## Technologies used

- HTML5
- CSS3 (Grid, Flexbox, custom properties, keyframe animations)
- JavaScript (ES6)
- `localStorage` for saving data in the browser
- GitHub Pages for deployment

## How to run

1. Download or clone this repository.
2. Open `index.html` in any modern browser. No installation or server is needed.

```bash
git clone https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git
cd YOUR-REPO-NAME
```

## Admin login (demo)

| Username | Password |
|---|---|
| `admin` | `admin123` |

## Project structure

```
├── index.html   # page structure, views and dialog
├── style.css    # layout, colours, responsive rules and animations
├── app.js       # data, validation, tracking, admin panel logic
└── README.md
```

## How it works

- `app.js` keeps all requests in one array and saves it to `localStorage` after every change.
- The same field and validation code is used by the student form and the admin edit dialog.
- The fee is calculated as: route base fare x number of months x (1 - discount).
- On first load the app adds a few sample requests so the dashboard is not empty.

## Limitations and future scope

- Data is stored in the browser's `localStorage`, so requests are visible only on the same browser and device. A real deployment would use a backend and database (for example Firebase or Node.js with MongoDB).
- The admin login is a demo check on the client side. A real system needs server-side authentication.
- Possible additions: student login, email notifications, online fee payment, and printable pass with a QR code.
