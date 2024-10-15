# 0x09. React Redux Connectors and Providers

## Overview

This project is designed to deepen your understanding of Redux connectors and providers within a React application. By the end of this project, you will be able to explain key Redux concepts and implement them in a React application without external assistance.

## Learning Objectives

- Understand [Redux connectors](https://react-redux.js.org/api/connect) and their usage.
- Learn the functions you can pass to a connector, such as `mapStateToProps` and `mapDispatchToProps`.
- Map an action creator to a component using a connector.
- Map an async action creator to a component with [Redux Thunk](https://redux-toolkit.js.org/api/createAsyncThunk).
- Set up your app’s store using [Redux Providers](https://react-redux.js.org/api/provider).
- Improve a connector’s performance using [Reselect](https://github.com/reduxjs/reselect).
- Use Redux’s [dev tools](https://chrome.google.com/webstore/detail/redux-devtools/lmhkpmbekcpmfncggjmhcmjkmfikpibp?hl=en) to debug the state of your application.

## Requirements

- Allowed editors: vi, vim, emacs, [Visual Studio Code](https://code.visualstudio.com/).
- All files should end with a new line.
- A `README.md` file at the root of the project folder is mandatory.
- All files will be interpreted/compiled on Ubuntu 18.04 LTS using [Node 12.x.x](https://nodejs.org/en/blog/release/v12.0.0/) and [npm 6.x.x].
- Push all files, including `package.json` and `.babelrc`.
- All functions must be exported.

## Provided Files

- `dashboard/dist/courses.json`
- `dashboard/dist/login-success.json`
- `dashboard/dist/notifications.json`

## Tasks

### Task 0: Write `mapStateToProps`

- Reuse the latest dashboard project from the React course.
- Install [`react-redux`](https://www.npmjs.com/package/react-redux).
- Create a function named `mapStateToProps` in `App/App.js`.
- Connect `mapStateToProps` to the component using `connect` from Redux.

### Task 1: Create a Small Store

- In `index.js`, create a store using `createStore` from Redux.
- Implement a provider passing the store to the main App.

### Task 2: Test `mapStateToProps`

- Export `mapStateToProps` and create a test suite in `App.test.js`.

### Task 3: Update `mapStateToProps`

- Update `mapStateToProps` to pass `displayDrawer` to the component.

### Task 4: Connect Your Action Creators

- Connect action creators `displayNotificationDrawer` and `hideNotificationDrawer` in `App.js`.

### Task 5: Refactor Your Code

- Remove old functions and state properties related to the drawer in `App.js`.
- Define `propTypes` and `defaultProps`.

### Task 6: Update Your Tests

- Refactor `App.test.js` to support the new attributes.

### Task 7: Async Actions & Thunk Middleware

- Install [`redux-thunk`](https://www.npmjs.com/package/redux-thunk) and apply the middleware in `index.js`.

### Task 8: Connect `LoginRequest` to the App

- Connect the action creator `loginRequest` in `App/App.js`.

### Task 9: Connect User State to the Footer

- Create `mapStateToProps` in `Footer/Footer.js` and connect the component.

### Task 10: Connect Logout Action Creator to the Header

- Connect the `logout` action creator in `Header/Header.js`.

### Task 11: Modify the `uiReducer`

- Update the `uiReducer` to handle `LOGIN` and `LOGOUT` actions.

### Task 12: Modify the Test Suites

- Update test suites for the components and `uiReducer`.

### Task 13: Understand How to Use the Redux Chrome Extension

- Install and configure the [Redux DevTools extension](https://chrome.google.com/webstore/detail/redux-devtools/lmhkpmbekcpmfncggjmhcmjkmfikpibp?hl=en).

### Task 14: Combine Store: Root Reducer

- Create `reducers/rootReducer.js` to combine all reducers.

### Task 15: Combine Store: Modify the Application

- Use the root reducer in `index.js`.

### Task 16: Combine Store: Write the Tests

- Update test suites to work with the new reducer format.

### Task 17: Connect Notifications: New Action Creator

- Add action creators in `notificationActionCreators.js`.

### Task 18: Connect Notifications: Improve Reducer

- Update `notificationReducer.js` to handle new actions.

### Task 19: Connect Notifications to the Reducer

- Map notifications state and actions in `Notifications.js`.

### Task 20: Connect Notifications: Clean Up

- Remove old functions and test data in `App.js`.

### Task 21: Connect Notifications: Update the Test Suites

- Update test suites for notifications and actions.

### Task 22: Selectors

- Use selectors to improve performance in `Notifications.js`.

### Task 23: Connect Courses: Create a Course Selector

- Create a course selector in `selectors/courseSelector.js`.

### Task 24: Connect Courses: Create a Fetch Courses Function

- Implement `fetchCourses` in `courseActionCreators.js`.

### Task 25: Connect the Courses Component

- Connect `CourseList.js` to actions and state.

### Task 26: Memoized Selectors: Redux Reselect

- Create a memoized selector in `notificationSelector.js`.

### Task 27: Memoized Selectors: Update the UI

- Update `Notifications` component to use the new selector.

### Task 28: Memoized Selectors: Update the Test Suite

- Add tests for the new selector and actions.

### Task 29: Container/Component

- Refactor `Notifications` into a container and component.

## Repository Structure

- **GitHub repository**: alx-react
- **Directory**: 0x09-react_redux_connectors_and_providers

## Conclusion

This project will enhance your skills in managing state with Redux in a React application, optimizing performance with selectors, and debugging with Redux DevTools. By completing these tasks, you will gain a comprehensive understanding of Redux connectors and providers.
