# 🐾 PetStore API Testing Project

## 📌 Overview
This project contains automated API tests for the **PetStore API** using Postman.

It demonstrates REST API testing skills including CRUD operations, positive/negative scenarios, and response validation using JavaScript test scripts.

---

## 🔗 API Source
https://petstore.swagger.io/

---

## 🧪 Test Coverage

### ✔ CRUD Operations
- Create a pet (POST)
- Get pet by ID (GET)
- Update pet (PUT)
- Delete pet (DELETE)

### ✔ Validation Includes
- Status code checks (200, 400, 404, 405)
- Response body validation
- JSON schema structure checks
- Field validation (id, name, category, status)
- Array validation (photoUrls, tags)
- Negative test scenarios

---

## ⚙️ Tools & Technologies
- Postman
- JavaScript (test scripts)
- REST API
- Swagger PetStore API

---

## 📂 Collection Content

- AddPet – create new pet and validate response
- UpdateAnExistingPet – update pet data
- FindPetById – get pet by ID
- FindPetsByStatus – filter pets by status
- DeletePet – remove pet by ID
- Negative test cases – invalid data & error handling

---

## 🧾 Example Test Script

```javascript
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});

pm.test("Check pet name", function () {
    const jsonData = pm.response.json();
    pm.expect(jsonData.name).to.eql("Тузік");
});
