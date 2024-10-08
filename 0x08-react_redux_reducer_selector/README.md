# 0x08. React Redux Reducer + Selector

## Project Overview

This project is focused on building Redux reducers and selectors, with a specific emphasis on maintaining immutability and using Normalizr for data normalization. By the end of this project, you will be able to explain the purpose of a reducer, its role in a Redux application, the importance of immutability, and the role of selectors.

### Learning Objectives
- Understand the purpose and role of a reducer within a Redux application.
- Learn why reducers must remain pure functions.
- Recognize the importance of avoiding state mutations in reducers.
- Implement **Immutable.js** in reducers for better immutability.
- Use **Normalizr** to simplify handling normalized state in your application.
- Create selectors to access state efficiently.

---

## Project Requirements

- All files should be interpreted/compiled on **Ubuntu 18.04 LTS** using **node 12.x.x** and **npm 6.x.x**.
- All your files should end with a new line.
- **Visual Studio Code**, `vi`, `vim`, or `emacs` are allowed editors.
- Push all necessary files, including `package.json` and `.babelrc`.
- All functions must be exported.

---

## Tasks

### 0. Write a Basic Reducer

#### Objective:
- Reuse the latest **dashboard project** from **0x08-React_Redux_action_creator+normalizr**.
- Create a UI reducer for managing application state related to UI elements.

#### Steps:
1. Define the initial state of the UI reducer in `reducers/uiReducer.js`:
   - `isNotificationDrawerVisible`: Boolean, set to `false`.
   - `isUserLoggedIn`: Boolean, set to `false`.
   - `user`: Object, initially empty.
   
2. Create the reducer function `uiReducer`:
   - Handle the following actions imported from `uiActionTypes`:
     - `DISPLAY_NOTIFICATION_DRAWER`: Set `isNotificationDrawerVisible` to `true`.
     - `HIDE_NOTIFICATION_DRAWER`: Set `isNotificationDrawerVisible` to `false`.
     - `LOGIN_SUCCESS`: Set `isUserLoggedIn` to `true`.
     - `LOGIN_FAILURE` and `LOGOUT`: Set `isUserLoggedIn` to `false`.

#### Testing:
- Write tests in `reducers/uiReducer.test.js` to:
  - Verify initial state when no action is passed.
  - Verify state when unrelated actions (e.g., `SELECT_COURSE`) are passed.
  - Ensure the reducer correctly handles `DISPLAY_NOTIFICATION_DRAWER`.

---

### 1. Use Immutable for the UI Reducer

#### Objective:
- Update the basic reducer to use **Immutable.js** for better immutability management.

#### Steps:
1. Install **Immutable.js** and import `Map` from it.
2. Replace the initial state with an Immutable `Map`.
3. Update the reducer to use `set` from `Map` for immutability.
4. Modify tests to account for Immutable.js state.

#### Requirements:
- Do not use `fromJS` or `toJS` in the reducer for better performance.

---

### 2. Create a Reducer for Courses

#### Objective:
- Create a new reducer to handle a list of courses.

#### Steps:
1. Define `FETCH_COURSE_SUCCESS` in `courseActionTypes`.
2. Write the `courseReducer.js`:
   - Default state should be an empty array.
   - When `FETCH_COURSE_SUCCESS` is dispatched, populate the state with courses and add an `isSelected` attribute (set to `false` for each course).
3. Define actions for selecting/unselecting a course (`SELECT_COURSE`, `UNSELECT_COURSE`).
4. Write tests in `courseReducer.test.js` to verify correct behavior for each action.

---

### 3. Create the Reducer for Notifications

#### Objective:
- Create a new reducer to manage notifications and filters.

#### Steps:
1. Define `FETCH_NOTIFICATIONS_SUCCESS` in `notificationActionTypes`.
2. Write the `notificationReducer.js`:
   - Default state includes `notifications` (empty array) and `filter` (set to "DEFAULT").
   - When `FETCH_NOTIFICATIONS_SUCCESS` is dispatched, populate `notifications` and set `isRead` to `false`.
   - Implement actions to mark a notification as read (`MARK_AS_READ`) and set a filter (`SET_TYPE_FILTER`).
3. Write tests in `notificationReducer.test.js`.

---

### 4. Normalizr & Immutable

#### Objective:
- Simplify state management using **Normalizr** and enhance immutability with **Immutable.js**.

#### Steps:
1. Create schema files for courses and notifications in `schema/courses.js` and `schema/notifications.js`.
2. Normalize the data in the reducers using the Normalizr schema.
3. Update the reducers to use **Immutable.js** for better state handling.
4. Update the tests to reflect the changes in state structure.

---

### 5. Selectors

#### Objective:
- Create selectors to efficiently access the state in the notifications reducer.

#### Steps:
1. Create the following selectors in `selectors/notificationSelector.js`:
   - `filterTypeSelected`: Returns the current filter value.
   - `getNotifications`: Returns the list of notifications.
   - `getUnreadNotifications`: Returns unread notifications.
2. Write tests for selectors in `selectors/notificationSelector.test.js`.

---

## Folder Structure

```
project-directory/
│
├── src/
│   ├── reducers/
│   ├── actions/
│   ├── schema/
│   ├── selectors/
│   └── tests/
│
├── package.json
├── .babelrc
└── README.md
```

---

## Running the Project

### Install Dependencies:
```
npm install
```

### Running Tests:
```
npm test
```
