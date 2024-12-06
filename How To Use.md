# 🌟 Redirect to Local Server Chrome Extension 🌟  

This is a powerful Chrome extension designed to simplify the workflow for developers working with live frontend applications and local backend servers. By enabling seamless redirection of API requests from the live frontend to your local server.

With this extension, developers can bypass the need for tools like Postman and Insomnia to test and debug API requests. Instead, you can test, debug, and integrate local backend server directly within your browser while maintaining the full functionality of a live frontend. 🚀  

---
## 🎯 Key Features:
1. Seamlessly connect your live frontend to a local server for real-time API testing.
2. Eliminate the need for tools like Postman or Insomnia by directly handling API requests in your browser.
3. Use placeholders (#) to dynamically support paths and query parameters for flexible redirection.
4. Redirect a group of APIs with a single placeholder (#) for easier management.
5. Control which APIs and features are active with simple ON/OFF buttons for the extension.
---

## 🎯 How to Add a Redirect  
1. **Click on the Yellow (+) icon**.  
2. Enter the following details:  
   - **From URL**: The live/staging API URL (e.g., `https://live-server-api.com/api/users`).  
   - **To URL**: Your local server URL (e.g., `http://localhost:3000/api/users`).  
   - **Method**: Choose the HTTP method (GET, POST, etc.).  
3. Click **Add Redirect**.  
4. Use the **ON/OFF Toggle buttons** to control the Extension and APIs.  
5. When APIs are redirected to the local server, a **blue popup message** will appear in the bottom-right corner.  

---

## 📚 Examples: Redirecting Requests  

### Example 1: Basic Redirects  
| **From URL**                    | **To URL**                        | **Method** |
|----------------------------------------|-------------------------------------------|------------|
| `https://live-server-api.com/api/add`     | `http://some-other-server/api2/add2`   | GET        |
| `https://live-server-api.com/api/users`   | `https://localhost:3000/api/users`    | GET        |
| `https://live-server-api.com/api/update`  | `http://localhost:5000/api/update`   | PUT        |
| `https://live-server-api.com/api/remove` | `http://localhost:3000/api/remove` | DELETE     |

---

### Example 2: Handling Dynamic Path and Query Parameters with Placeholders (`#`)  
Redirects with placeholders let you dynamically match and replace parts of the URL.  

| **Live URL (From)**                       | **Local URL (To)**                     | **Method** |
|-------------------------------------------|----------------------------------------|------------|
| `https://live-server-api.com/api/user/#/profile` | `http://localhost:3000/api/user/#/profile` | GET    |
| `https://live-server-api.com/api/item?id=#` | `http://localhost:3000/api/item?id=#` | DELETE   |

#### **How This Works**  
  If the live URL is `GET https://live-server-api.com/api/user/123/profile`, the request will be redirected to `GET http://localhost:3000/api/user/123/profile`.  
- The `#` symbol acts as a **placeholder** for dynamic values (e.g., Path and Query Parameters).  

---

### Example 3: Redirect Multiple APIs with Patterns  
You can redirect **multiple APIs** with a single pattern.  

| **From URL**              | **To URL**               | **Method** |
|----------------------------------|----------------------------------|------------|
| `https://live-server-api.com/api/#` | `http://localhost:3000/api/#`| GET        |
| `https://live-server-api.com/#submit` | `http://localhost:3000/#submit` | POST    |

#### **How This Works**  
- **Example 1:**  
  Any URL starting with `https://live-server-api.com/api/` will redirect to `http://localhost:3000/api/`.  
  - `GET https://live-server-api.com/api/orders` → `GET http://localhost:3000/api/orders`  
  - `GET https://live-server-api.com/api/products/123` → `GET http://localhost:3000/api/products/123`  

- **Example 2:**  
  Any URL ending with `/submit` will redirect:  
  - `POST https://live-server-api.com/orders/submit` → `POST http://localhost:3000/orders/submit`  
  - `POST https://live-server-api.com/admin/selling/submit` → `POST http://localhost:3000/admin/selling/submit`
  - `POST https://live-server-api.com/admin/projectsubmit` → `POST http://localhost:3000/admin/projectsubmit` 

---

## 🔧 Troubleshooting Tips  
- Make sure your **local server is running** and accessible.  
- Verify that the **From URL**, **To URL**, and **Method** are correctly configured.  
- Use **Developer Tools → Network Tab** in your browser to check if requests are redirected properly.  

---

### 📧 Need Help?  
Email me at **svfodekar@gmail.com** for any assistance.  
