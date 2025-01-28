---
title: Installation
sidebar_label: Installation
sidebar_position: 2
---

Welcome to the GreekMyth Web App! This guide will walk you through the steps to set up and run GreekMyth locally on your machine using XAMPP.

## Project Structure

[Github Repository](https://github.com/ZenithSUS/finalProject_ITEC116)

The repository consists of three main folders:

1. **GreekMyth CMS**: Admin dashboard for managing the content of the website.
2. **GreekMyth Website**: User-facing platform for interaction and story sharing.
3. **API**: Acts as the bridge connecting the GreekMyth CMS and the GreekMyth Website.

## Prerequisites

Before you begin, ensure you have the following installed on your device:

- XAMPP (PHP and MySQL environment)
- A modern web browser (e.g., Chrome, Firefox, Edge)

## Installation Steps

### Step 1: Clone the Repository

1. Open your terminal or command prompt.
2. Clone the repository using the following command:

```bash title="bash or cmd"
git clone https://github.com/ZenithSUS/finalProject_ITEC116.git
```

3. Once cloned, navigate to the project directory:

```bash title="bash or cmd"
cd finalProject_ITEC116
```

### Step 2: Move Folders to XAMPP's htdocs

1. Locate your XAMPP installation folder. The default path is typically:

- Windows: C:\xampp\htdocs

2. Copy the following folders from the cloned repository into the htdocs directory:

- finalProject_ITEC116

### Step 3: Set Up the Database

1. Start XAMPP and ensure Apache and MySQL services are running.
2. Open your browser and go to:

```
http://localhost/phpmyadmin
```

3. Create a new database:

- Click on New in the left-hand menu.
- Name your database (e.g., greekmyth) and click Create.

4. Import the SQL file:

- Inside the main folder, locate the SQL file (e.g., greekmyth.sql).
- Go to the database you created in phpMyAdmin.
- Click Import and select the corresponding SQL file.

## Troubleshooting

- If the website or CMS doesn’t load, ensure that:
  - Apache and MySQL are running in XAMPP.
  - The folders are placed correctly in htdocs.
  - Database configurations (config.php) match your setup.
- If you encounter a database error, check if you’ve imported the SQL files into the correct database.
