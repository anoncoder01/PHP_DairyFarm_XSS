**Affected Web App:** Dairy Farm Shop Management System in PHP

**Software Link:** [Dairy Farm](https://phpgurukul.com/dairy-farm-shop-management-system-using-php-and-mysql/#google_vignette)

**Version:** v1.1

**Title:** Stored Cross Site Scripting (XSS) vulnerability

**Affected Component:** /add-product.php, /edit_product.php
<br> pname parameter within each of these files is vulnerable to stored Cross-Site Scripting

**Impact:** Cross-Site Scripting (XSS) vulnerability is a serious web security threat. When attackers execute this type of threat by injecting malicious scripts, it can lead to user data being compromised, their account getting hijacked or even malware getting installed on the host machine.

**Image:**

<img width="913" alt="vulnerability1" src="https://github.com/user-attachments/assets/0a2a34a8-fd0f-488f-b526-f47dfd93d953"> 

<img width="906" alt="vulnerability2" src="https://github.com/user-attachments/assets/fff3f608-f437-4858-9834-633c04bf7c22">


**Proof of Concept:** To reproduce this attack, an attacker can inject a script into the Product Name field either while adding new products or editing new products (as shown in the two figures above) under the Product tab of the application. The payload '<script>alert(1)</script>' was successfully accepted, leading to an alert being triggered for the user when the products are being viewed in mange_products.php


<img width="907" alt="vulnerability_proof" src="https://github.com/user-attachments/assets/17039174-5e72-4d13-9550-57a086db5f54">


**Remediation:** It is important to update Dairy Farm Shop Management System by properly sanitizing code variables and including restrictions for special characters so that malicious input such as the one showed in the example cannot be injected.
