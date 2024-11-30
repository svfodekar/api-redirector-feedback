# Redirect to Local Server Chrome Extension

## Overview
This extension helps backend developers redirect API requests from a live frontend to their **local development server**. It makes debugging and testing frontend features with the local backend seamless.

---

## How to Add a Redirect
1. **Click Add (+)**.
2. Enter the following:
   - **From URL**: The live/staging API URL you want to redirect (e.g., `https://live-api.com/api/users`).
   - **To URL**: Your local server URL (e.g., `http://localhost:3000/api/users`).
   - **Method**: Choose the HTTP method (GET, POST, etc.).
3. Click **Add Redirect**.
4. Use Toggle buttons to control Extension and APIs. 
5. When apis are being redirect to local server you will see blue popup message at right bottom corner.

---

## Examples: Redirecting Requests

### Example 1: Basic Redirects
| **Live URL (From)**                           | **Local URL (To)**                        | **Method** |
|-----------------------------------------------|-------------------------------------------|------------|
| `GET https://live-api.com/api/add`           | `GET http://some-other-server/api2/add`      | GET       |
| `GET https://live-api.com/api/users`          | `GET https://localhost:3000/api/users`     | GET        |
| `PUT https://live-api.com/api/update/some`     | `PUT http://localhost:5000/api/update/some`| PUT        |
| `DELETE https://live-api.com/api/remove/me`  | `DELETE https://localhost:3000/api/remove/me` | DELETE |

### Example 2: Handling Dynamic Path and Query Parameters with Placeholders (`#`)
Redirects with placeholders let you dynamically match and replace parts of the URL.

| **Live URL (From)**                              | **Local URL (To)**                          | **Method** |
|--------------------------------------------------|---------------------------------------------|------------|
| `GET https://live-api.com/api/user/#/profile`    | `GET http://localhost:3000/api/user/#/profile` | GET      |
| `DELETE https://live-api.com/api/item?id=#`      | `DELETE http://localhost:3000/api/item?id=#`  | DELETE   |

#### How This Works:
- **Example:**  
  If the live URL is `GET https://live-api.com/api/user/123/profile`, the request will be redirected to `GET http://localhost:3000/api/user/123/profile`.
- The `#` symbol acts as a **placeholder** for dynamic values (e.g., Path and Query Parameters ).

### Example 3: Redirect Groups of APIs with Patterns
You can redirect **multiple APIs** with a single pattern.

| **Live URL (From)**                              | **Local URL (To)**                          | **Method** |
|--------------------------------------------------|---------------------------------------------|------------|
| `GET https://live-api.com/api/#`                 | `GET http://localhost:3000/api/#`           | GET        |
| `POST https://live-api.com/#/submit`             | `POST http://localhost:3000/#/submit`       | POST       |

#### How This Works:
- **Example 1:**  
  Any URL starting with `https://live-api.com/api/` will be redirected to `http://localhost:3000/api/`.
  - `GET https://live-api.com/api/orders` → `GET http://localhost:3000/api/orders`
  - `GET https://live-api.com/api/products/123` → `GET http://localhost:3000/api/products/123`

- **Example 2:**  
  Any URL ending with `/submit` will be redirected:
  - `POST https://live-api.com/orders/submit` → `POST http://localhost:3000/orders/submit`
  - `POST https://live-api.com/selling/admin/submit` → `POST http://localhost:3000/selling/admin/submit`

---

## Troubleshooting Tips
- Make sure your **local server is running** and accessible.
- Verify that the **From URL** , **To URL** , **Method** are correctly configured.
- Use **Developer Tools → Network Tab** in your browser to check if requests are redirected properly.

**Email me at svfodekar@gmail.com if need help with how to use extension** 
