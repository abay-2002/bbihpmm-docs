# Login

:::info

Learn how to **Login**.

:::

```jsx title="/src/components/HelloCodeTitle.js"
function HelloCodeTitle(props) {
  return <h1>Hello, {props.name}</h1>;
}
```

## 1. Navigate to Login Page
- The user opens the application and is presented with a login page or login modal.
- If the user is not logged in, they are typically redirected to the login page upon trying to access protected resources.

## 2. Enter Credentials
- The user enters their **email** and **password** in the respective fields.
  - The email should be in a valid format (e.g., `user@example.com`).
  - The password field should hide the characters for privacy.

## 3. Submit Login Form
- The user clicks the **Login** button or presses **Enter** to submit their credentials.
- The system validates that the form is not empty and checks if both fields are filled correctly.

## 4. Validate Credentials
- The backend verifies the user's credentials:
  - **Check if the email exists** in the database.
  - **Compare the password** provided by the user with the hashed password stored in the database.
  - If the email or password is incorrect, the user is notified with an error message (e.g., "Invalid email or password").

## 5. Generate Session or Token
- If the credentials are correct:
  - A session ID (for session-based authentication) or a JWT (JSON Web Token) is generated.
  - This session ID/token is stored in a **cookie** or returned in the response.

## 6. Redirect User
- If the login is successful:
  - The user is redirected to their **dashboard** or home page.
  - If the user was trying to access a protected route before logging in, they are redirected back to that route after logging in.

## 7. Error Handling (if needed)
- If login fails:
  - The user is shown an error message such as "Invalid credentials" or "Account locked" (if applicable).
  - Provide an option for the user to retry or reset their password.

## 8. Optional: Two-Factor Authentication (2FA)
- If 2FA is enabled, the user may be prompted for an additional code sent to their email or phone.

## 9. Logout Option
- Once logged in, the user can access their account and settings.
- The user can choose to **log out** at any time, which will invalidate the session/token and redirect them to the login page.
