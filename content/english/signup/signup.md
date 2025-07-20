---
title: "Sign Up"
date: 2025-07-20T12:00:00+00:00
draft: false
---

Welcome to our signup page! Please fill the form below:

<form name="signup" method="POST" data-netlify="true" netlify-honeypot="bot-field" action="/thank-you/">
  <input type="hidden" name="form-name" value="signup">

  <label for="name">Full Name:</label><br>
  <input type="text" id="name" name="name" required><br><br>

  <label for="email">Email:</label><br>
  <input type="email" id="email" name="email" required><br><br>

  <label for="password">Password:</label><br>
  <input type="password" id="password" name="password" required><br><br>

  <label>Gender:</label><br>
  <input type="radio" id="male" name="gender" value="Male" required>
  <label for="male">Male</label>
  <input type="radio" id="female" name="gender" value="Female">
  <label for="female">Female</label><br><br>

  <label for="age">Age:</label><br>
  <input type="number" id="age" name="age" min="10" max="120" required><br><br>

  <button type="submit">Sign Up</button>
</form>
