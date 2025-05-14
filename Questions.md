# React, API Handling, and Playwright Review

## Instructions

This review is divided into two parts. It contains 15 multiple-choice questions in total.

## Section 1: Error Handling with try-catch and API Calls in React

**1. In React, when making an API call using `fetch`, where is the most appropriate place to put a `try-catch` block?**
    A) Outside the component function.
    B) Directly inside the JSX returned by the component.
    C) Around the `fetch` call and the subsequent promise handling (e.g., `.then(res => res.json())`).
    D) Only around the state update functions (e.g., `setData(response)`).

**2. What is the primary purpose of a `try-catch` block when fetching data from an API in a React component?**
    A) To speed up the API request.
    B) To handle potential errors during the API call or data processing, preventing the app from crashing.
    C) To automatically retry the API call if it fails.
    D) To replace the need for `useState` for managing API data.

**3. In a `try-catch` block, what does the `catch` part receive as an argument?**
    A) The successfully fetched data.
    B) An error object if an exception occurs in the `try` block.
    C) A boolean indicating if the `try` block was successful.
    D) The URL of the API endpoint.

**4. If you want to display a user-friendly error message when an API call fails, where would you typically set the state for this message?**
    A) Inside the `try` block, before the API call.
    B) Inside the `catch` block.
    C) Outside the `try-catch` block, after it has executed.
    D) Directly in the JSX without using state.

**5. Which of the following is a good practice when handling errors from an API call in React?**
    A) Always reload the entire page when an error occurs.
    B) Displaying a generic "An error occurred" message without logging details.
    C) Logging the error to the console for debugging and displaying a user-friendly message to the UI.
    D) Ignoring errors in development and only handling them in production.

## Section 2: Managing Loading States with `useState`

**6. How do you typically initialise a `useState` variable for tracking loading status?**
    A) `const [isLoading, setIsLoading] = useState(null);`
    B) `const [isLoading, setIsLoading] = useState(true);` or `const [isLoading, setIsLoading] = useState(false);` (depending on initial state)
    C) `const isLoading = useState(false);`
    D) `const [isLoading] = useState('pending');`

**7. When should you set `isLoading` to `true` in the context of an API call?**
    A) After the API call is successful.
    B) After an error occurs in the API call.
    C) Just before making the API call.
    D) Only if the API call takes longer than 5 seconds.

**8. When should `isLoading` typically be set back to `false`?**
    A) Immediately after setting it to `true`.
    B) Only if the API call results in an error.
    C) After the API call has completed (either successfully or with an error) and data processing (or error handling) is done.
    D) Never, it should remain `true` to indicate data has been loaded.

**9. How can you use the `isLoading` state variable in your JSX?**
    A) `<div>{isLoading}</div>`
    B) `<button disabled={isLoading}>Submit</button>`
    C) ` {isLoading ? <p>Loading...</p> : <DataDisplay data={data} />} `
    D) Both B and C.

**10. Why is it important to manage an `isLoading` state?**
    A) It's required by React for `useState` to function.
    B) It improves the user experience by providing feedback during asynchronous operations.
    C) It helps in debugging API calls.
    D) It makes the API calls faster.

## Section 3: Basic Playwright Testing

**11. What is a primary use case for Playwright in web development?**
    A) To write CSS styles.
    B) To manage application state.
    C) To perform end-to-end (E2E) and UI testing by automating browser interactions.
    D) To bundle JavaScript code for production.

**12. How would you typically start writing a Playwright test for a webpage?**
    A) By importing React components directly into the test file.
    B) By using `test('test name', async ({ page }) => { /* test code */ });`
    C) By writing plain JavaScript functions without any specific test runner syntax.
    D) By using `console.log` to check page elements.

**13. In Playwright, how can you check if a specific text string is visible on the page?**
    A) `await page.checkText('Welcome to our app');`
    B) `await expect(page.getByText('Welcome to our app')).toBeVisible();`
    C) `await page.find('Welcome to our app');`
    D) `console.assert(page.includes('Welcome to our app'));`

**14. What does `await page.goto('/')` typically do in a Playwright test?**
    A) It closes the browser page.
    B) It navigates the current browser page to the root URL of the application being tested.
    C) It takes a screenshot of the current page.
    D) It reloads the current page.

**15. You want to ensure a page header (e.g., an `<h1>` tag) contains the text "Product Details". Which assertion would be most appropriate?**
    A) `await expect(page.locator('h1')).toHaveText('Product Details');`
    B) `await page.header.includes('Product Details');`
    C) `expect(page.getByRole('heading', { level: 1, name: 'Product Details' })).toHaveAttribute('type', 'text/css');`
    D) `await page.locator('h1').isVisible('Product Details');`
