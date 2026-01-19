# Arduino for All – CS50 Final Project

#### Video Demo: https://www.youtube.com/watch?v=_T4QUeYI4Lo

## Description

Hello, my name is Rubens. I am from Brazil and I live in the state of Minas Gerais. I am a programmer, and while thinking about my final project for CS50, I came up with the idea for **Arduino for All**.

I have a personal goal of creating an electronics, computer, and robotics laboratory, but I currently have limited resources and equipment. I started by teaching small programming classes using Arduino, but the lack of equipment made it difficult to expand.

The idea of this project is to create a website that allows people to donate electronic equipment to schools that want to build laboratories to teach programming and electronics. Through the platform, schools can register and request items, while donors can offer smartphones, computers, laptops, and other electronic devices that they no longer use.

The project was developed focusing on two main types of users: **Donors**, who want to donate unused devices, and **Schools**, which can use these donations to create maker labs and teach programming and electronics.

---

## Website Features

### Donors can:
- Register on the website
- Log in
- Access a map showing all registered schools
- Select a school and view its details
- Donate items requested by a school
- Change their password
- View their donation history
- View their ranking position
- Log out

### Schools can:
- Log in
- View the history of received donations
- Mark donations as received
- Log out

### The Administrator can:
- Register new schools
- Update existing school information
- Remove schools from the system

When a donation is made, the donor only receives points after the school confirms that the equipment was received. The ranking system is based exclusively on confirmed donations.

---

## Database Tables

### schools
Stores information about schools.
Fields: id, name, address, city, state, country, phone, email, password, latitude, longitude, photo

### users
Stores donor information.
Fields: id, name, email, password, photo

### items
Contains all items that schools can request, along with the score assigned to each item.
Fields: id, name, description, icon, scores

### school_items
Lists the items that each school wants to receive.
Fields: id, school_id, item_id

### donations
Stores all donations made by users and their status.
Fields: id, user_id, school_id, item_id, amount, received

---

## Technologies Used

This project was built using **Flask (Python)**, **SQLite3** for the database, **JavaScript**, and **SASS** for styling.

I implemented features such as secure password hashing, image upload with filename sanitization, an administration panel for managing schools, and advanced SQL queries to calculate user rankings and donation points.

## Future Improvement

Migrate password hashing to Werkzeug security helpers.

---

## Conclusion

Developing this project from scratch using Flask was a very valuable learning experience. I explored many new concepts and technologies that I had never worked with before. I spent a significant amount of time studying, testing, and refining the code before implementing each feature.

This project helped me consolidate my knowledge in web development, databases, and backend programming, and I am very satisfied with the final result.
