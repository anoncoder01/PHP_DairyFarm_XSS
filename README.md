Affected Web App: Dairy Farm Shop Management System in PHP

Version: v1.1

Title: Stored Cross Site Scripting (XSS) vulnerability

Affected Component: /add_product.php, /edit_product.php

Impact: Cross-Site Scripting (XSS) vulnerability is a serious web security threat, allowing attackers to inject malicious scripts with diverse impacts. Users face data theft, session hijacking, and unwittingly performing unauthorized actions.

Proof of Concept: To reproduce this attack, an attacker can inject a script into the Product Name field either while adding new products or editing new products under the Product tab of the application. The payload '<script>alert(1)</script>' was successfully accepted, leading to an alert being triggered for the user

Image:


Remediation: It is important to update Dairy Farm Shop Management System by properly sanitizing code variables and including restricting for special characters so that malicious input such as the one showed in the example cannot be injected. 
