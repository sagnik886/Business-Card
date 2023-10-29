<script>
  let cardColor = "pink";
  let textColor = "black";
  let fontFamily = "Arial, sans-serif"; // Default font style
  let fontSize = "16px"; // Default font size
  let message = "Your Message";

  let src = "https://encrypted-tbn1.gstatic.com/images?q=tbn:ANd9GcR23n_YfedRHX-JrUhf1lfj1D2sWgPKia3lr2-vYGdl6-TW20pq";
  let alt = "random img";

  function changeBack(newColor) {
      cardColor = newColor;
  }

  function changeText(newColor) {
      textColor = newColor;
  }

  function changeFont(newFont) {
      fontFamily = newFont;
  }

  function changeFontSize(newSize) {
      fontSize = newSize;
  }

  function updateMessage(event) {
      message = event.target.value;
  }
</script>

<main>
  <div class="nav">
      <h1>Create Unique Business Cards!</h1>
      <img {src} {alt} />
  </div>

  <div class="body">
      <div class="info">
          <div class="info1">
              <label for="colorSelect">Back Color:</label>
              <select id="colorSelect" bind:value={cardColor} on:change={() => changeBack(cardColor)}>
                  <option value="lightblue">Light Blue</option>
                  <option value="pink">Pink</option>
                  <option value="lightgreen">Light Green</option>
                  <option value="lightyellow">Light Yellow</option>
              </select>
          </div>

          <div class="info1">
              <label for="textColorSelect">Text Color:</label>
              <select id="textColorSelect" bind:value={textColor} on:change={() => changeText(textColor)}>
                  <option value="black">Black</option>
                  <option value="red">Red</option>
                  <option value="green">Green</option>
                  <option value="white">White</option>
              </select>
          </div>

          <div class="info1">
              <label for="fontSelect">Font Style:</label>
              <select id="fontSelect" bind:value={fontFamily} on:change={() => changeFont(fontFamily)}>
                  <option value="Arial, sans-serif">Arial</option>
                  <option value="Helvetica, sans-serif">Helvetica</option>
                  <option value="Times New Roman, serif">Times New Roman</option>
                  <option value="Courier New, monospace">Courier New</option>
              </select>
          </div>

          <div class="info1">
              <label for="fontSizeSelect">Font Size:</label>
              <select id="fontSizeSelect" bind:value={fontSize} on:change={() => changeFontSize(fontSize)}>
                  <option value="12px">Small</option>
                  <option value="16px">Medium</option>
                  <option value="20px">Large</option>
                  <option value="24px">Extra Large</option>
              </select>
          </div>

          <div class="info1">
              <label for="messageInput">Business name:</label>
              <input type="text" id="messageInput" bind:value={message} on:input={updateMessage} />
          </div>
      </div>

      <div class="card">
          <div class="card1" style="background-color: {cardColor}; color: {textColor}; font-family: {fontFamily}; font-size: {fontSize};">
              <p>{message}</p>
          </div>
      </div>
  </div>
</main>

<style>
  *{
      width: 100%;
      padding: 0;
      margin: 0;
      text-decoration: none;
      box-sizing: border-box;
      background-color: #e6e6e6;
  }

  h1{
      color: rgb(147, 96, 206);
      /* background-color: #fac769; */
      font-size: 3rem;
      text-align: center;
  }

  .nav{
      width: 100%;
      height: 250px;
      background-color: #fac769;
      display: flex;
      flex-direction: row;
      justify-content: center;
      align-items: center;
  }

  img{
      width: 40%;
      height: 100%;
  }

  .body{
      width: 100%;
      /* height: 100vh; */
      margin-top: 1.5rem;
      padding: 2rem;
      background-color: #e6e6e6;
  }

  .info{
      width: 100%;
      padding: 1.5rem;
      /* margin-bottom: 2rem; */
      border: 1px solid rgba(0, 0, 0, 0.162);
      /* box-shadow: 1px 1px 1px rgb(101, 97, 97);          */
      display: flex;
      flex-direction: row;
      justify-content: space-evenly;
      align-items: center;
      flex-wrap: wrap;
      
  }

  .info1{
      width: 35%;
  }

  label{
      font-size: 1.5rem;
      font-weight: 500;
  } 

  select{
      font-size: 1.2rem;
      font-weight: 500;
      padding: 0.75rem;
      margin: 0.75rem;
      border-radius: 0.5rem;
      border: 2px solid black;
      background-color: white;
  }

  input{
      font-size: 1.2rem;
      font-weight: 500;
      padding: 0.75rem;
      margin: 0.75rem;
      font-size: 1.2rem;
      border-radius: 0.5rem;
      border: 2px solid black;
      background-color: white;
  }

  .card{
      width: 100%;
      display: flex;
      flex-direction: row;
      justify-content: center;
      align-content: center;
  } 

  .card1{
    width: 370px;
    height: 250px;
    border: 5px solid rgba(150, 135, 135, 0.171);
    margin: 3rem;
    padding: 2rem;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  p{
    background-color: transparent;
    text-align: center;
  }
</style>
