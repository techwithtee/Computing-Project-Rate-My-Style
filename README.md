# Rate My Style

A fashion rating web application built with ASP.NET Web Forms and C#, developed as a Foundation Year Computing project — awarded a First.

## Overview

Rate My Style is a community-driven platform where users can share their outfits and rate each other's fashion choices. Users register for an account, upload images of their garments with details like item type, colour, shop, and price, and browse other users' styles to rate them out of five.

## Features

- **User Registration & Login** — Secure account creation with username/password authentication; users are redirected back to the login page after successful registration
- **Browse Styles** — A gallery page displaying all uploaded garment images, each clickable to view full details and leave a rating
- **Rate Outfits** — Users can rate any garment on a scale of 1–5, with their existing rating displayed on return visits
- **Upload Garments** — Authenticated users can upload a photo of their outfit alongside item details (name, colour, shop, price), which are saved to the database and image store
- **Session Management** — User sessions are maintained across pages; logout returns the user to the homepage

## Pages

| Page | Description |
|---|---|
| `HomePage.aspx` | Landing page with featured outfit images and a login prompt |
| `Login.aspx` | Authentication page with login and register options |
| `Registration.aspx` | New user sign-up form collecting first name, last name, email, username, and password |
| `Styles.aspx` | Authenticated gallery showing all uploaded garments as clickable images |
| `Rate.aspx` | Individual garment detail page showing item info and a 1–5 star rating form |
| `Upload.aspx` | Form for uploading a new outfit image with associated garment metadata |

## Tech Stack

- **Language:** C# (.NET Framework 4.8)
- **Framework:** ASP.NET Web Forms
- **Database:** Microsoft Access (`.accdb`) via OleDb
- **IDE:** Visual Studio (`.sln` / `.csproj` project files included)

## Database Schema

The application uses a Microsoft Access database (`RateStyle.accdb`) with three tables:

- **Registration** — stores user accounts (`ID`, `FirstName`, `LastName`, `Email`, `Username`, `Password`)
- **Garments** — stores uploaded outfit entries (`ID`, `Item`, `Colour`, `Shop`, `Price`, `Image`)
- **Rating** — stores user ratings per garment (`Rate`, `GID` [Garment ID], `RID` [Rater's User ID])

## Getting Started

### Prerequisites

- Windows OS
- Visual Studio (2019 or later recommended)
- IIS Express (included with Visual Studio)
- Microsoft Access Database Engine (ACE OLEDB 12.0 driver) — [download here](https://www.microsoft.com/en-us/download/details.aspx?id=54920)

### Running the Project

1. Clone or download this repository
2. Open `RateMyStyle_Tee.sln` in Visual Studio
3. Ensure the Microsoft ACE OLEDB 12.0 driver is installed on your machine
4. Press **F5** or click **Run** to launch the application via IIS Express
5. The app will open at `HomePage.aspx` — register a new account to get started

> **Note:** The database file (`RateStyle.accdb`) is included in the project. No additional database setup is required.

## Project Structure

```
RateMyStyle-master/
├── RateMyStyle_Tee.sln
└── RateMyStyle_Tee/
    ├── HomePage.aspx / .cs
    ├── Login.aspx / .cs
    ├── Registration.aspx / .cs
    ├── Styles.aspx / .cs
    ├── Rate.aspx / .cs
    ├── Upload.aspx / .cs
    ├── RateStyle.accdb          # Access database
    ├── Images/                  # Uploaded garment images
    ├── Properties/
    ├── Web.config
    └── packages.config
```

## Academic Context

This project was developed as part of a Foundation Year Computing course and was awarded a First Class grade. It demonstrates core concepts including database-driven web development, user authentication, session handling, file uploads, and CRUD operations with SQL via OleDb.
