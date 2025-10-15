---
title: "Serialization and Deserialization in Java"
datePublished: Wed Oct 15 2025 00:23:10 GMT+0000 (Coordinated Universal Time)
cuid: cmgr8z4mw000002jmct5c7ybt
slug: serialization-and-deserialization-in-java
tags: shreenibas

---

## 🧩 **Serialization and Deserialization in Java**

### 🔹 **Definition**

* **Serialization** → Converting a **Java object into a data format** (like JSON, XML, or byte stream) for transmission or storage.
    
* **Deserialization** → Converting that **data format back into a Java object**.
    

These are used widely in **API testing (Rest Assured)**, **file storage**, **network communication**, and **Java object persistence**.

---

## 🔹 **Why It’s Important in API Automation**

* To **send** Java objects as **JSON/XML** in the API request (Serialization).
    
* To **read** API responses (JSON/XML) and map them back to **Java POJOs** for validation (Deserialization).
    
* Makes tests **type-safe**, **clean**, and **maintainable**.
    

---

## 🔹 **Commonly Used Libraries in Java**

| Library | Description | Common Use |
| --- | --- | --- |
| **Jackson (com.fasterxml.jackson)** | Most popular, default in Rest Assured | Converts between Java objects and JSON |
| **Gson (**[**com.google**](http://com.google)**.gson)** | Lightweight, easy to use | Used in Android and simple JSON APIs |
| **Json-B / Eclipse Yasson** | Jakarta EE (Java EE 8+) JSON binding | For enterprise Java apps |
| **org.json** | Simple JSON parser | Manual parsing (less common in automation) |
| **Jackson Databind** | Core of Jackson library | Handles both serialization and deserialization |

✅ **Rest Assured uses Jackson by default** if it’s on the classpath.

---

## 🔹 **Universal Example (Works with Rest Assured or Plain Java)**

### Step 1: Create a POJO class

```java
public class User {
    private String name;
    private int age;
    private String email;

    // Getters and Setters
    public String getName() { return name; }
    public void setName(String name) { this.name = name; }

    public int getAge() { return age; }
    public void setAge(int age) { this.age = age; }

    public String getEmail() { return email; }
    public void setEmail(String email) { this.email = email; }
}
```

---

### Step 2: **Serialization (Object → JSON)** using Jackson

```java
import com.fasterxml.jackson.databind.ObjectMapper;

User user = new User();
user.setName("Nini");
user.setAge(25);
user.setEmail("nini@test.com");

ObjectMapper mapper = new ObjectMapper();
String json = mapper.writeValueAsString(user);   // ✅ Java → JSON
System.out.println(json);
```

**Output:**

```java
{"name":"Nini","age":25,"email":"nini@test.com"}
```

---

### Step 3: **Deserialization (JSON → Object)**

```java
String jsonString = "{\"name\":\"Nini\",\"age\":25,\"email\":\"nini@test.com\"}";

User userObj = mapper.readValue(jsonString, User.class);  // ✅ JSON → Java
System.out.println(userObj.getEmail());
```

---

### Step 4: **Using in Rest Assured**

**Serialization (sending Java object as body):**

```java
given()
    .contentType("application/json")
    .body(user)    // Rest Assured automatically serializes using Jackson
.when()
    .post("/createUser")
.then()
    .statusCode(201);
```

**Deserialization (converting response to POJO):**

```java
User userResponse = 
    given()
        .get("/getUser/101")
    .then()
        .extract()
        .as(User.class);   // Rest Assured uses Jackson to deserialize
```

---

## 🔹 **Advanced Notes for Interviews**

| Concept | Explanation |
| --- | --- |
| **Default Mapper** | Rest Assured uses **Jackson** automatically if present in Maven dependencies. |
| **Switching Library** | You can switch to Gson: `RestAssured.config = RestAssured.config().objectMapperConfig(objectMapperConfig().defaultObjectMapperType(ObjectMapperType.GSON));` |
| **Annotations** | Use `@JsonProperty`, `@JsonIgnore`, `@JsonInclude` to control JSON mapping. |
| **Custom Mapper** | You can create your own `ObjectMapper` for date formats or naming strategies. |
| **Serialization Exception** | Occurs if object contains unknown or unsupported types (e.g., circular references). |
| **Deserialization Exception** | Occurs if JSON fields do not match Java fields or are missing. |

---

## 🔹 **Common Interview Questions and Universal Answers**

| Question | Universal Answer |
| --- | --- |
| **1\. What is Serialization?** | Converting a Java object into JSON/XML or byte stream format. |
| **2\. What is Deserialization?** | Converting JSON/XML back into a Java object. |
| **3\. Why do we use it in Rest Assured?** | To send Java POJOs as request bodies and to map responses back into objects for easy validation. |
| **4\. Which library handles it by default?** | Jackson (in Rest Assured). |
| **5\. Can you use other libraries?** | Yes, like Gson, Json-B, or org.json. |
| **6\. What annotations are used for JSON mapping?** | `@JsonProperty`, `@JsonIgnore`, `@JsonInclude`, `@JsonFormat`. |
| **7\. How to handle mismatched field names?** | Use `@JsonProperty("actual_json_field")`. |
| **8\. What is ObjectMapper?** | A class in Jackson used for manual serialization/deserialization. |
| **9\. What happens if a field is missing in JSON?** | Jackson ignores it by default unless configured otherwise. |
| **10\. Can we serialize nested objects or lists?** | Yes, Jackson handles nested and collection types automatically. |

---

✅ **In short (Universal 2-line Interview Answer):**

> *“Serialization is converting a Java object into JSON or XML so it can be sent to an API, and Deserialization is converting JSON or XML back into a Java object. In Rest Assured, this happens automatically using Jackson or Gson libraries, which helps in sending clean requests and validating structured responses.”*