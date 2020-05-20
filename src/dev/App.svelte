<script>
  import QrCode from '../lib/index.svelte';  
</script>


<main class="container">
  <div class="content">
    <h1>This is your <strong>Boarding pass</strong></h1>
    <div class="resume">
      <div class="fly">
        <div class="row">
          <div class="local">
            <p>Brazil</p>
            <h2>BRA</h2>
          </div>
          <img src="./assets/images/icon.png" alt="" />
          <div class="local">
            <p>Amsterdam</p>
            <h2>AMS</h2>
          </div>
        </div>
        <div class="info-group">
          <div class="items">
            <p>Name</p>
            <h3 class="name">Jonas Alves</h3>
          </div>
          <div class="items">
            <p>seat</p>
            <h3>12A</h3>
          </div>
          <div class="items">
            <p>gate</p>
            <h3>20C</h3>
          </div>
        </div>
      
        <div class="info-group">
          <div class="items">
            <p>Boarding time</p>
            <h3>11:00</h3>
          </div>
          <div class="items">
            <p>Departure</p>
            <h3>14:00</h3>
          </div>
          <div class="items">
            <p>Arruval</p>
            <h3>16:00</h3>
          </div>
        </div>
      </div>
      <div class="sidebar">
        <div class="info-group">
          <div class="items">
            <p>Name</p>
            <h3 class="name">RS 7593</h3>
          </div>
          <div class="items">
            <p>Date</p>
            <h3>{new Date().toDateString()}</h3>
          </div>
        </div>
        <QrCode class="qrcode" value="https://www.linkedin.com/in/jonas-alves-9163a5136/"/>
      </div>
    </div>
  </div>
</main>

<style>
  .container {
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .content {
    max-width: 850px;
    width: 100%;
    background: #fff;
    border-radius: 10px;
    margin: 20px;
    padding: 56px 40px;
    box-shadow: 0px 13px 97px rgba(0, 0, 0, 0.17);
  }
  h1 {
    font-size: 24px;
    font-weight: normal;
  }
  h1, h2, h3, p {
    color: #1D1D28;
  }
  .resume {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
  }
  .fly {
    margin-top: 88px;
  }
  .fly {
    flex: 1;
  }
  .row {
    display: flex;
    justify-content: space-between;
    margin-bottom: 48px;
    max-width: 500px;
  }
  .row img {
    width: 60px;
    height: 48px;
  }
  .local p {
    font-size: 16px;
    color: #40404B;
  }
  .local h2 {
    font-size: 50px;
    color: #1D1D28;
  }
  .info-group {
    display: flex;
    justify-content: space-between;
    margin-top: 40px;
    max-width: 500px;
  }
  .items:nth-child(2){
    text-align: center;
  }
  .items:nth-child(3){
    text-align: right;
  }
  .items p {
    font-size: 14px;
    font-weight: bold;
    text-transform: uppercase;
    color: #8C8B92;
    text-align: left
  }
  .items h3 {
    font-size: 24px;
    color: #1C1D23;
  }
  .items h3.name {
    color: #4b4ad5;
    text-align: left;
  }
  .sidebar {
    padding: 0 60px;
  }
  .sidebar .info-group {
    display: block;
  }
  .sidebar :global(.qrcode) {
    width: 200px;
  }
  .sidebar .items {
    margin-bottom: 40px;
    
  }

  @media (max-width: 720px) {
    .resume {
      flex-direction: column-reverse;
    }
    .fly {
      margin-top: 48px;
    }
    .sidebar {
      width: 100%;
      margin-top: 40px;
      display: flex;
      padding: 0;
      justify-content: space-between;
      flex-wrap: wrap;
    }
  }
</style>