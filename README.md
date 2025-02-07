# Groupie-Tracker-Visualizations

## Objectives

- We must follow the same principles as the first subject.

- Groupie tracker visualizations consists of manipulating the data coming from the API and displaying it in the most presentable way possible to you.
- The Schneiderman's 8 Golden Rules of Interface Design must be followed:

- **Strive for consistency**
- **Enable frequent users to use shortcuts**
- **Offer informative feedback**
- **Design dialogue to yield closure**
- **Offer simple error handling**
- **Permit easy reversal of actions**
- **Support internal locus of control**
- **Reduce short-term memory load**

## Principles of first subject

- Receiv a given API and manipulate the data contained in it in order to create a website displaying the information.

- Using the given API, that is made up of four parts:

- **Artists: Contains information about some bands and artists like their name(s), image, in which year they began their activity, the date of their first album and the members.**

- **Locations: Contains their last and/or upcoming concert locations.**

- **Dates: Contains their last and/or upcoming concert dates.**

- **Relation: Links the data of all the other parts, artists, dates and locations.**

- Given all this, we built a user-friendly website which can display the band's info through several data visualizations.

- This project also focuses on the creation and visualization of events/actions.

---

## Project Structure

```
    groupie-tracker-visualizations/
    ├── server.go               # Main application server
    ├── server_test.go
    ├── go.mod
    ├── utils/
    │   ├── errors.go
    │   ├── pagehandler.go
    │   ├── readfromapi.go
    │   ├── saferender.go
    │   └── structs.go
    ├── templates/
    │   ├── index.html
    │   ├── head.html
    │   ├── badRequest.html
    │   ├── internalServer.html
    │   ├── navBar.html
    │   ├── goBackButton.html
    │   └── notFound.html
    └── static/
        ├── index.html
        └── css/
            ├── styles.css
            └── index.html
```

## Usage

### How to Run

1. Clone this repository to your local machine:
   ```bash
   git clone https://01.gritlab.ax/git/tdideric/groupie-tracker-visualizations.git
   ```
2. Navigate to the project directory:
   ```bash
   cd groupie-tracker-visualizations
   ```
3. Ensure you have Go installed (version 1.19+ recommended).

4. Run the application:

   ```bash
   go run .

   ```

5. Open your browser and navigate to http://localhost:8080

---

## Instructions

1. Browse through the page to select a band or use the search bar.
2. Select either "See Details" at search bar or "More Information" under the artist picture.
3. Check the artist page.
4. Go back to main paige by either "Go back button" or using the header in the nav-bar

---

- Routes:

  - /:
    - Renders the homepage using the index.html template.
    - Serves static CSS files for styling.
  - /artist/<artist_name>:
    - Renders the artist details using the MoreInformationPage.html template.
    - Serves static CSS files for styling.

- Error Handling:
  - Custom HTML templates (badRequest.html, notFound.html, internalServer.html) are served for HTTP error codes.

---

## Authors

- Mohammad mahdi Kheirkhah
- Fatemeh Kheirkhah
- Toft Diederichs

---
