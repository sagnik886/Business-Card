<main>
	<div class="nav">
		<div class="nav1">
			<h1>Find the perfect Business card template</h1>
		</div>

		<div class="nav2">
			<h1>Making a Business card is easy. Create from a template tailored just for you. Start for free!</h1>
		</div>
	</div>

	<div class="body">
		<div class="search">
			<div class="search1">
              <label for="name">Business name</label>
							<input type="text" id="name" placeholder="Enter your business name">
      </div>

			<div class="search2">
              <label for="keywords">Keywords</label>
							<input type="text" id="keywords" placeholder="Search by keyword">
      </div>

			<button type="submit">SEARCH</button>
		</div>

		<div class="template">
			<div class="item" id="item1">
				<div class="item1-img">
					<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAOEAAADhCAMAAAAJbSJIAAAAV1BMVEX///9kZGReXl5ubm6ZmZn8/PyIiIhYWFhhYWFdXV1lZWXw8PD39/d3d3fh4eFZWVl/f3+RkZG3t7fU1NRqamrAwMCtra2dnZ3Hx8dSUlKioqLb29u8vLxgbJhkAAACdklEQVR4nO3bbW+qMBiA4bautKgI+DZx+/+/80DBI77sRHOq8LD7+rBkhJjeKfBkU5UCAAAAAAAAAAAAAAAAAAAAAAAAAAAAAEi3LtdDL+G1EmdcMvQiXmiZGa21yZZDL+RVFlszrwvnZrsYeikvYK1aea9b3q+aA1OzyU+BdWK+GXo58e2c7nO7oRcU2941O2hCXfPTu/3QS4rrM+xgtc689tm6Crv4OfSi4rEqSUPTQc3qwpk6hN40UVN52rRjMDxd2sLuqTOZwbiYNzler9TfQrXS4dh8EoOxHYNmtmiuya7QqsXM6HkYjOJt6nturtOiveVOe1hHFml9XDvxg7Eeg3VHXna/nguVKvOmXfJgbHZt7y4HQ7+wGyFhMMp8qNpew6mgX2h7/TILVTcGq8P5yMUeKnWousEokT2NwbT/LLkqVJv0NBgF7uJiG0aeuZgH14VqZcJZIv9iLEw3BvtuCsNgrM8r3rm0OGy4w7Kri++2UNks3K0Cr9LSeVdeH7xT+MOZ42ftsVjfPD/uFVq1Lo4C/6lxf8V39/Af58vzc+FUUCgfhfJRKB+F8lEoH4XyUSgfhfJRKB+F8lEoH4XyUSgfhfJRKB+F0tmucCrv995T1IUCP1iiunfhH9iaL+fcV7yXe6fv4vjQR5qXX4+ddiy+/29Bse0qn8f8/F2S+2pcHzwtvdZpvMvKplqbj2gvF0PyKwpNxEJD4dtR+CQKB0DhkygcAIVPonAAFD5ppIW/4G+LpY1lOc491D41cbRfaBthYVwjKyzN1AsPVaQL9Kz/1dMxOHzENrJAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAEDPHyU/GRrNtN1zAAAAAElFTkSuQmCC" alt="" width="75" height="75"/>
				</div>

				<div class="item1-info">
					<p class="item1-info-head">Upload your logo</p>
					<p class="item1-info-para">
							<label for="logoUpload">Click on me:</label>
              <input type="file" id="logoUpload" accept=".jpg, .jpeg, .png" bind:files={selectedLogo} />
					</p>
				</div>
			</div>
			
			<div class="item">2</div>
			<div class="item">3</div>
			<div class="item">4</div>
			<div class="item">5</div>
			<div class="item">6</div>
			<div class="item">7</div>
			<div class="item">8</div>
			<div class="item">9</div>
			<div class="item">10</div>
			<div class="item">11</div>
			<div class="item">12</div>
			<div class="item">13</div>
			<div class="item">14</div>
			<div class="item">15</div>
			<div class="item">16</div>
			<div class="item">17</div>
			<div class="item">18</div>
			<div class="item">19</div>
			<div class="item">20</div>
			<div class="item">21</div>
			<div class="item">22</div>
			<div class="item">23</div>
			<div class="item">24</div>
			<div class="item">25</div>
	</div>
</main>


<script>
    let selectedLogo = null;

    async function handleLogoUpload() {
        if (selectedLogo) {
            const formData = new FormData();
            formData.append('logo', selectedLogo);

            try {
                const response = await fetch('/upload-logo', {
                    method: 'POST',
                    body: formData,
                });

                if (response.ok) {
                    console.log('Logo uploaded successfully.');
                    // You can add further actions after a successful upload
                } else {
                    console.error('Logo upload failed.');
                }
            } catch (error) {
                console.error('Network error:', error);
            }
        } else {
            console.error('No file selected.');
        }
    }
</script>


<style>
    *{
        font-family: sans-serif;
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }

	.nav{
		width: 100%;
		height: 368px;
		/* background-color: yellow; */
		/* color: red; */
		background-image: linear-gradient(rgb(0,0,0),rgb(88,88,88));
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.nav1 h1{
		font-size: 3.2rem;
		font-weight: 500;
        font-family: sans-serif;
		text-align: center;
		color: white;
		margin: 0px 0px 8px;
	}

	.nav2 h1{
		font-size: 1.5rem;
        font-weight: 400;
        font-family: sans-serif;
		text-align: center;
		color: #D0D0D0;
		margin: 16px 0px;
	}

	.body{
		width: 100%;
		/* height: 100vh; */
		background-color: #F4F4F4;
		padding: 48px 0px 0px;
	}

	.search{
		display: flex;
		flex-direction: row;
		justify-content: space-evenly;
		align-items: center;
		flex-wrap: wrap;
		border: 1px solid rgb(208 208 208);
		padding: 16px 24px;
		margin: 0px 32px;
		background-color: rgb(239 239 239);
	}

	.search1{
		display: flex;
		flex-direction: row;
	    justify-content: flex-start;
		align-items: center;
		margin-right: 20px;
	}

	.search2{
		display: flex;
		flex-direction: row;
	    justify-content: flex-start;
		align-items: center;
		margin-right: 20px;
	}

	button{
		background-color: #F21B3F;
        color: white;
        border: none;
        border-radius: 0.25rem;
        font-size: 14px;
		font-weight: 700;
		width: 90px;
		height: 48px;
	}

	.search1 label{
		margin-right: 20px;
        color: #5e5e5e;
		font-size: 16px;
		font-weight: 550;	
        font-family: sans-serif;
	}

	.search2 label{
		margin-right: 20px;
        color: #5e5e5e;
		font-size: 16px;
		font-weight: 550;	
        font-family: sans-serif;
	}

	.search1 input{
		padding: 12px;
		width: 324px;
		height: 48px;
		border: 1px solid rgb(208 208 208);
        font-family: sans-serif;
	}

	.search2 input{
		padding: 12px;
		width: 324px;
		height: 48px;
		border: 1px solid rgb(208 208 208);
        font-family: sans-serif;
	}

	.template{
		padding: 32px 32px 16px 32px;
		display: grid;
		grid-template-rows: repeat(5,1fr);
		grid-template-columns: repeat(5,1fr);
		grid-gap: 1.25rem;
		place-items: center;	
	}

	.item{
		width: 100%;
	    height: 160px;
		border: 1px solid black;
        border-radius: 0.25rem;
	}

	.item:hover{
		transform: scale(1.02);
		box-shadow: 0 0 transparent;
	}

	#item1{
		display: flex;
		flex-direction: row;
		justify-content: space-evenly;
		align-items: center;
		border: 1.7px dashed rgb(208 208 208);
        background-color: white;
	}

    #item1:hover{
        background-color: #F4F4F4;
    }

	.item1-info{
		font-size: 14px;
	}

	.item1-info-head{
		margin-bottom: 8px;
		font-weight: 550;
	}

	.item1-info-para input{
		display: none;
	}

	.item1-info-para label{
		color: blue;
	}
	
</style>
