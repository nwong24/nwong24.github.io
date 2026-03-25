---
layout: essay
type: essay
title: "Final Project Proposal"
date: 2026-03-24
labels:
  - Software Engineering
  - Nextjs
---
# Project: Manoa Book Swap

### Overview (Proposers: Nathan Wong)
_The Problem_: After finishing a semester, students can be left with physical textbooks they have no more use for. In addition, students taking classes next semester might have to buy a brand new textbook which can be expensive.

_The Solution_: Our app Manoa Book Swap will allow students to sell and buy used textbooks from each other, leading to less waste and more savings each semester.

### Approach
This app will allow users to coordinate meetups with each other where they can sell or give away their used physical textbooks. The two roles that will exist are the admins, who are trusted students who can make changes to the site's list of classes and textbooks, and student users, who can create listings or search for listings. 

Users will be able to log in and create listings by entering a textbook’s ISBN number and the book's condition and their asking price.
Users will be able to log in and also look for listing for a textbook they want that semester.
Admins will be able to add classes and their associated textbooks to allow users to filter by their class number.

Some possible mockup pages include:
- Landing Page
- User Home Page
- Admin Home Page
- Admin list of users
- List of available books
- Page to add a book to sell
- Page to search books (filter)
- Page that shows what books you are currently selling
- Page that shows which books you are looking for (bookmarked)
- Profile pages for a certain user
- Chat between buyer and seller

### Use case ideas
User goes to landing page, logs in, adds a listing for a book to sell.
User goes to landing page, logs in, goes to the page of books, searches for their desired book.
User gets a notification that a book they are looking for has been added to the market.
User gets a notification that someone is willing to buying their book.
Admin goes to landing page, logs in, goes to list of users, views a user.
Admin goes to landing page, logs in, adds a class and its textbooks to the site.

### Beyond the basics
- Verification system where students can upload their UH ID which admins will manually verify to get another layer of trust.
- An AI agent that autonomously scans UH course catalogs and publicly available syllabi such as the [ICS syllabi](https://courses.ics.hawaii.edu/syllabuses) that can automatically generate courses and textbooks.
- Adding an option to pay through the app instead of having the students coordinate payment with each other
- AI suggested price listed based on condition of the book
- Review and rating system for sellers and buyers (5 star system)
