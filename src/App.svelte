<script>
	let name = '';
	let title = '';
	let company = '';
	let countryCode = '';
	let phoneNumber = '';
	let email = '';
	let address = '';
	let website = '';
  
	function handleSubmit() {
	  if(validateForm()){
		alert('Submitted!')
	  }
	  if (!validateForm()) {
		alert('Please fill out all required fields correctly.');
		return;
	  }
  
	  // You can handle form submission here, e.g., send the data to a server
	  console.log('Form submitted:', { name, title, company, phoneNumber: `${countryCode} ${phoneNumber}`, email, address, website });
	}
  
	function validateForm() {
	  // Validate that countryCode and phoneNumber contain only '+', '0', '1', '2', '3', '4', '5', '6', '7', '8', '9'
	  return (
		name &&
		email &&
		address &&
		countryCode.match(/^[\+\d]+$/) &&
		phoneNumber.match(/^[\d]+$/) &&
		phoneNumber.length >= 10 &&
		countryCode.length <= 4
	  );
	}
  </script>
  
  <style>
	/* Add your responsive CSS styles here */
	.form-container {
	  max-width: 400px;
	  margin: 0 auto;
	  padding: 20px;
	  border: 1px solid #ccc;
	  border-radius: 10px;
	  background-color: #f9f9f9;
	  font-family: 'Arial', sans-serif;
	}
  
	.title {
	  font-size: 24px;
	  font-weight: bold;
	  text-align: center;
	  margin-bottom: 20px;
	  color: #007bff;
	  cursor: pointer;
	}
  
	.title:hover {
	  text-decoration: underline;
	}
  
	label {
	  display: block;
	  margin-top: 10px;
	  font-weight: bold;
	  color: #333;
	}
  
	input,
	textarea {
	  width: 100%;
	  padding: 10px;
	  margin-top: 5px;
	  border: 1px solid #ccc;
	  border-radius: 5px;
	  font-size: 16px;
	  color: #555;
	}
  
	button {
	  background-color: #007bff;
	  color: #fff;
	  padding: 10px 20px;
	  border: none;
	  border-radius: 5px;
	  cursor: pointer;
	  margin-top: 20px;
	  font-size: 18px;
	  font-weight: bold;
	}
  
	button:hover {
	  background-color: #0056b3;
	}
  
	/* Add more CSS for responsive design as needed */
  </style>
  
  <div class="form-container">
	<div class="title">The Business Card Generator: Input Form</div>
	<form on:submit={handleSubmit}>
	  <label for="name">Name</label>
	  <input type="text" id="name" bind:value={name} required />
  
	  <label for="title">Title</label>
	  <input type="text" id="title" bind:value={title} />
  
	  <label for="company">Company</label>
	  <input type="text" id="company" bind:value={company} />
  
	  <label for="countryCode">Country Code</label>
	  <input type="tel" id="countryCode" bind:value={countryCode} />
  
	  <label for="phoneNumber">Phone Number</label>
	  <input type="tel" id="phoneNumber" bind:value={phoneNumber} required />
  
	  <label for="email">Email</label>
	  <input type="email" id="email" bind:value={email} required />
  
	  <label for="website">Website</label>
	  <input type="url" id="website" bind:value={website} />
  
	  <label for="address">Address</label>
	  <textarea id="address" bind:value={address} required></textarea>
  
	  <button type="submit">Generate Business Card</button>
	</form>
  </div>

/* HTML file */ 

    <!DOCTYPE html>
    <html lang="en">

<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<link rel="stylesheet" href="style.css">
	<title>Contact us Page</title>
</head>

<body>
	<!-- Header section -->
	<header>
		<button class="hamburger" id="hamburger-icon">
			<span onclick="openNavbar()"> ☰</span>
		</button>
		<div class="logo">Your Logo</div>
		<nav id="nav-menu">
			<ul>
				<li><a href="#">Home</a></li>
				<li><a href="#">Enquiry</a></li>
				<li><a href="#">About</a></li>
				<li><a href="#">Services</a></li>
			</ul>
		</nav>
		<button class="reachUs-button">Call us</button>
	</header>

	<!-- banner section -->
	<section class="banner">
		<img src="forms1.jpg"
			alt="Welcome to our page">
	</section>

	<!-- Contact form -->
	<section class="contact-form">
		<div class="form-container">
			<h2>Your Details</h2>
			<form action="#" method="POST">

				<label for="name">Name: </label>
				<input type="text" id="name" name="name" required>

                <label for="title">Title: </label>
				<input type="text" id="title" name="title" required>

                <label for="company">Company: </label>
				<input type="text" id="company" name="company" required>

				<label for="email">Email: </label>
				<input type="email" id="email" name="email" required>

				<label for="phone">Phone: </label>
				<input type="tel" id="phone" name="phone">

				<label for="address">Address: </label>
				<textarea id="text" name="address" rows="4" required></textarea>

				<button type="submit" class="submit-button">Submit</button>
			</form>
		</div>
	</section>


	/* CSS */
	<style>
	*{
		margin: 0;
		padding: 0;
		box-sizing: border-box;
	}
	
	body {
		font-family: Arial, sans-serif;
		line-height: 1.6;
	}
	
	/* Header styles */
	header {
		display: flex;
		justify-content: space-between;
		align-items: center;
		padding: 20px;
		background-color: #ca5252;
		color: white;
		height: 4rem;
	}
	
	.logo {
		font-size: 2rem;
	}
	
	nav {
		width: 30rem;
	}
	
	nav ul {
		list-style: none;
		display: flex;
		justify-content: space-between;
	}
	
	nav ul li a {
		font-size: 1.2rem;
		padding: 1rem;
		text-decoration: none;
		color: white;
	}
	
	nav ul li a:hover {
		background-color: #ffffff;
		border: none;
		border-radius: 4px;
		cursor: pointer;
	}
	.reachUs-button {
		padding: 1rem;
		background-color: white;
		border: none;
		color: #e36969;
		border-radius: 4px;
		cursor: pointer;
	}
	.reachUs-button:hover{
		background-color: #f0a6a6;
	}
	
	/* banner section styles */
	.banner {
		text-align: center;
		background-color: #ffffff;
		margin: 0 auto;
	}
	
	.banner img {
		padding: 1rem;
		max-width: 20%;
		height: auto;
	}
	/* Contact form styles */
	.contact-form {
		padding: 40px 0;
		margin: 0 10px;
	}
	
	.form-container {
		max-width: 40%;
		margin: 0 auto;
		padding: 50px;
		background-color: #ffffff;
		border-radius: 10px;
		box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
	}
	
	.contact-form h2 {
		text-align: center;
		margin-bottom: 20px;
	}
	
	.form-group {
		margin-bottom: 20px;
	}
	
	.form-container label {
		display:block;
		font-weight: bold;
	}
	.form-container input, textarea{
		width: 100%;
		padding: 10px;
		border: 1px solid #ccc;
		border-radius: 4px;
		margin-bottom: 1rem;
		resize: vertical;
	}
	.submit-button {
		padding: 10px 20px;
		background-color: #e36969;
		border: none;
		color: white;
		border-radius: 4px;
		font-size: 1rem;
		cursor: pointer;
	}
	
	/* Contact info styles */
	.contact-info {
		text-align: center;
		padding: 50px 0;
		background-color: #f7f7f7;
	}
	
	.contact-info h2 {
		margin-bottom: 20px;
	}
	
	/* Footer styles */
	footer {
		padding: 20px;
		text-align: center;
		background-color: #333;
		color: white;
	}
	/* Hamburger styles */
	.hamburger {
		display: none;
		color: rgb(0, 0, 0);
		font-size: 1.5rem;
		cursor: pointer;
	}
	
	/* Media queries for responsiveness */
	@media only screen and (max-width: 768px) {
		.logo {
			display: none;
		}
	
		.hamburger {
			display: flex;
		}
	
		#nav-menu {
			position: absolute;
			top: 4rem;
			left: 0;
			background-color: #333;
			width: 100%;
			display: none;
		}
	
		#nav-menu.active {
			display: block;
			flex-direction: row;
			padding: 1rem;
		}
	}
</style>