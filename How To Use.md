# 🌟 Redirect to Local Server Chrome Extension 🌟  

This extension empowers backend developers to seamlessly redirect API requests from a live frontend to their local backend development server. It simplifies debugging and testing frontend/backend features with a local backend, making the development process faster and more efficient! 🚀  

---

## 🎯 How to Add a Redirect  
1. **Click on the Yellow (+) icon**.  
2. Enter the following details:  
   - **From URL**: The live/staging API URL (e.g., `https://live-api.com/api/users`).  
   - **To URL**: Your local server URL (e.g., `http://localhost:3000/api/users`).  
   - **Method**: Choose the HTTP method (GET, POST, etc.).  
3. Click **Add Redirect**.  
4. Use the **ON/OFF Toggle buttons** to control the Extension and APIs.  
5. When APIs are redirected to the local server, a **blue popup message** will appear in the bottom-right corner.  

---

## 📚 Examples: Redirecting Requests  

### Example 1: Basic Redirects  
| **Live URL (From)**                    | **Local URL (To)**                        | **Method** |
|----------------------------------------|-------------------------------------------|------------|
| `GET https://live-api.com/api/add`     | `GET http://some-other-server/api2/add`   | GET        |
| `GET https://live-api.com/api/users`   | `GET https://localhost:3000/api/users`    | GET        |
| `PUT https://live-api.com/api/update`  | `PUT http://localhost:5000/api/update`   | PUT        |
| `DELETE https://live-api.com/api/remove` | `DELETE http://localhost:3000/api/remove` | DELETE     |

---

### Example 2: Handling Dynamic Path and Query Parameters with Placeholders (`#`)  
Redirects with placeholders let you dynamically match and replace parts of the URL.  

| **Live URL (From)**                       | **Local URL (To)**                     | **Method** |
|-------------------------------------------|----------------------------------------|------------|
| `GET https://live-api.com/api/user/#/profile` | `GET http://localhost:3000/api/user/#/profile` | GET    |
| `DELETE https://live-api.com/api/item?id=#` | `DELETE http://localhost:3000/api/item?id=#` | DELETE   |

#### **How This Works**  
- **Example:**  
  If the live URL is `GET https://live-api.com/api/user/123/profile`, the request will be redirected to `GET http://localhost:3000/api/user/123/profile`.  
- The `#` symbol acts as a **placeholder** for dynamic values (e.g., Path and Query Parameters).  

---

### Example 3: Redirect Multiple APIs with Patterns  
You can redirect **multiple APIs** with a single pattern.  

| **Live URL (From)**              | **Local URL (To)**               | **Method** |
|----------------------------------|----------------------------------|------------|
| `GET https://live-api.com/api/#` | `GET http://localhost:3000/api/#`| GET        |
| `POST https://live-api.com/#submit` | `POST http://localhost:3000/#submit` | POST    |

#### **How This Works**  
- **Example 1:**  
  Any URL starting with `https://live-api.com/api/` will redirect to `http://localhost:3000/api/`.  
  - `GET https://live-api.com/api/orders` → `GET http://localhost:3000/api/orders`  
  - `GET https://live-api.com/api/products/123` → `GET http://localhost:3000/api/products/123`  

- **Example 2:**  
  Any URL ending with `/submit` will redirect:  
  - `POST https://live-api.com/orders/submit` → `POST http://localhost:3000/orders/submit`  
  - `POST https://live-api.com/admin/submit` → `POST http://localhost:3000/admin/submit`  

---

## 🔧 Troubleshooting Tips  
- Make sure your **local server is running** and accessible.  
- Verify that the **From URL**, **To URL**, and **Method** are correctly configured.  
- Use **Developer Tools → Network Tab** in your browser to check if requests are redirected properly.  

---

### 📧 Need Help?  
Email me at **svfodekar@gmail.com** for any assistance.  
