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
  