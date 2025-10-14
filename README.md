# Rest Assured Complete Note
<h3 align="left">📒 Notes & Resources For QA Automatation</h3>

<ul>
   <li><a href="https://github.com/shreenibassamal/hashnodeBlog-AutomationTesting-restAssured/blob/main/cmgqoiaex000002l46yz8c2hz.md">CHAPTER 01 Introduction</a></li>
    <li><a href=""></a></li> 
     <li><a href=""></a></li> 
      <li><a href=""></a></li> 
       <li><a href=""></a></li> 
        <li><a href=""></a></li> 
         <li><a href=""></a></li> 
          <li><a href=""></a></li> 
           <li><a href=""></a></li>
    <li><a href=""></a></li>
  
</ul>

## 🔹 **Basic REST Assured Interview Questions**

1. What is **Rest Assured**?
    
2. Why do we use Rest Assured in automation testing?
    
3. What is an **API**? What is the difference between REST and SOAP API?
    
4. What are the key features of REST architecture?
    
5. What is the **difference between GET, POST, PUT, DELETE, PATCH**?
    
6. What are the dependencies required to use Rest Assured in Maven?
    
7. How do you **set base URI and base path** in Rest Assured?
    
8. How to send a **GET request** using Rest Assured?
    
9. How to send a **POST request** with a JSON body?
    
10. What is the use of `given()`, `when()`, `then()` in Rest Assured?
    

---

## 🔹 **Intermediate-Level Questions**

11. How do you **add headers** in a request?
    
12. How to send **query parameters** and **path parameters**?
    
13. What is the difference between `param()` and `queryParam()`?
    
14. What is the difference between `pathParam()` and `queryParam()`?
    
15. How to send **authentication** in Rest Assured (Basic Auth, OAuth, Bearer Token)?
    
16. How to **validate status code** of a response?
    
17. How do you validate **response body** using Rest Assured?
    
18. How do you **extract data** from a JSON response?
    
19. How do you **log request and response details**?
    
20. How to handle **different content types** like JSON, XML, or text?
    

---

## 🔹 **Assertions & Validations**

21. How do you validate a specific **JSON key-value pair**?
    
22. How do you **verify response headers**?
    
23. What is the use of **Hamcrest matchers** in Rest Assured?
    
24. What is the difference between `assertThat()` and `body()` assertions?
    
25. How do you validate **response time**?
    
26. How do you **validate schema** of a response (JSON Schema Validation)?
    
27. What is **JSONPath** and how is it used in Rest Assured?
    
28. What is **XMLPath** and how is it used?
    
29. How do you handle **arrays or nested JSON** in response?
    
30. How do you verify if a response **contains a specific value**?
    

---

## 🔹 **Advanced-Level Questions**

31. What is **Chaining** in Rest Assured?
    
32. How to **extract token** from one API and use it in another API?
    
33. How to **send multiple requests in a flow** (like Login → Create → Get → Delete)?
    
34. How do you perform **data-driven API testing** using Rest Assured?
    
35. How can you **integrate Rest Assured with TestNG or JUnit**?
    
36. How do you use **RequestSpecification** and **ResponseSpecification**?
    
37. What is **given().spec()** used for?
    
38. How to use **Filters** in Rest Assured?
    
39. How to set **global baseURI** and **basePath** for all tests?
    
40. How to generate **Allure / Extent reports** for API tests?
    

---

## 🔹 **Authentication & Authorization**

41. What are the different **authentication mechanisms** supported by Rest Assured?
    
42. How to perform **Basic Authentication**?
    
43. How to perform **Digest Authentication**?
    
44. How to perform **Bearer Token Authentication**?
    
45. How to perform **OAuth 2.0 Authentication**?
    
46. How do you handle **JWT tokens** in Rest Assured?
    
47. How to send **API keys** in header or query param?
    
48. How to handle **expired tokens**?
    
49. What is the difference between **Authentication** and **Authorization**?
    
50. How to use **preemptive authentication** in Rest Assured?
    

---

## 🔹 **Error Handling & Response Codes**

51. What are the **commonly used HTTP status codes** and their meanings?
    
52. How to handle **404 / 500 errors** in Rest Assured?
    
53. How do you validate **different status codes** in one framework?
    
54. How do you handle **timeouts or failed responses**?
    
55. How do you **retry failed API requests** automatically?
    

---

## 🔹 **Real-time & Scenario-based Questions**

56. How do you validate an API response with **dynamic values**?
    
57. If one API’s output is input to another, how do you handle that in Rest Assured?
    
58. How do you validate a **JSON array** of objects (like a list of users)?
    
59. How do you test **file upload and download APIs**?
    
60. How do you handle **multipart/form-data** requests?
    
61. How to validate **pagination** in API responses?
    
62. How do you handle **environment-specific base URLs** (QA, Stage, Prod)?
    
63. How do you handle **API versioning**?
    
64. How do you **mock API responses**?
    
65. How do you integrate **Postman collections** with Rest Assured tests?
    

---

## 🔹 **Framework Design & Best Practices**

66. How do you design a **Rest Assured framework** in your project?
    
67. What packages do you include in your framework?
    
68. How do you **manage request payloads** (JSON files, POJOs, or maps)?
    
69. What is a **POJO class** and how is it used for serialization/deserialization?
    
70. How do you **read data from Excel or JSON** for API input?
    
71. How do you handle **test data management** in API automation?
    
72. How do you perform **parallel execution** of API tests?
    
73. How do you integrate your framework with **Jenkins**?
    
74. How do you trigger your API tests from **Maven** or **CI/CD pipeline**?
    
75. How do you maintain **reusable utilities** and **common methods**?
    

---

## 🔹 **Reporting & Integration**

76. How do you generate **Extent Report** for API tests?
    
77. How do you include **logs and screenshots** (if UI is involved)?
    
78. How do you send **test reports via email** after execution?
    
79. How to integrate Rest Assured tests with **Jenkins pipeline**?
    
80. How do you store **execution history or API results**?
    

---

## 🔹 **Miscellaneous / Tricky Questions**

81. What are **static imports** in Rest Assured and why are they used?
    
82. What’s the difference between `RestAssured.given()` and `given()`?
    
83. What’s the role of **Response** and **ValidatableResponse** interfaces?
    
84. What is **RequestSpecification** and why do we use it?
    
85. How to verify **null / empty responses**?
    
86. How to handle **cookies and sessions** in Rest Assured?
    
87. What is the use of `contentType()` and `accept()` methods?
    
88. What is **serialization and deserialization** in Rest Assured?
    
89. What’s the difference between `extract().path()` and `jsonPath().get()`?
    
90. How to set **proxy settings** for API testing?
    

---

## 🔹 **Practical / Coding-based Questions**

91. Write a Rest Assured script to **validate status code = 200**.
    
92. Write a **POST request** to create a user with a JSON body.
    
93. Write code to send a **GET request with path parameters**.
    
94. Write code to **extract a field value** from JSON response.
    
95. Write a code to **validate response time &lt; 2 seconds**.
    
96. Write a code to **send Bearer token authentication**.
    
97. Write a code to **chain two APIs** (login + get user).
    
98. Write a code for **JSON schema validation**.
    
99. Write a code for **parameterized API testing using TestNG DataProvider**.
    
100. Write a code for **handling dynamic path parameters**.
