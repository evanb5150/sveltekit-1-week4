<script>
	import Counter from './Counter.svelte';
	import welcome from '$lib/images/svelte-welcome.webp';
	import welcome_fallback from '$lib/images/svelte-welcome.png';
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
	<h1>
		<span class="welcome">
			<picture>
				<source srcset={welcome} type="image/webp" />
				<img src={welcome_fallback} alt="Welcome" />
			</picture>
		</span>

		to your new<br />SvelteKit app
	</h1>

	<h2>
		try editing <strong>src/routes/+page.svelte</strong>
	</h2>

	<Counter />
</section>

<div class="card" id="card"> 

    <div class="dup-btn">
  <button id="dup">Duplicate</button>
  </div>
    
    <h1> Drew Allar</h1>
  <div class="btn-image">
    <img src= "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR9pEBqeQ_41-Bf5E7eDYhWpRVVI1bAYUplYQ&usqp=CAU" alt = "Beaver Stadium"/>
         <p> Drew Allar</p> 
  </div>
  
  <div class="btn-wrapper">
     <button id="stat">Stats</button>
    <a href="https://gopsusports.com/sports/football/roster/drew-allar/13992"></a>
  </div>
  
  
  <div class="details-button">
    <button id="det">Details</button>
    <a href="https://hax.psu.edu/"></a>
  </div>
   
    </div>
  
  <script> document.querySelector('#dup').addEventListener('click', (e) => {
        
      let p = document.getElementById("card");
      let d = p.cloneNode(true);
      document.body.appendChild(d);
          });
  </script>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
	}

	h1 {
		width: 100%;
	}

	.welcome {
		display: block;
		position: relative;
		width: 100%;
		height: 0;
		padding: 0 0 calc(100% * 495 / 2048) 0;
	}

	.welcome img {
		position: absolute;
		width: 100%;
		height: 100%;
		top: 0;
		display: block;
	}

	.cards {
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    
  }
  
  .card-container {
    background-color: #001e44;
    width: 20%;
    height: 50%;
    display: block;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    border-radius: 10px;
  }
  
  
  .card-content {
    text-align: center;
    color: white;
    display: block;
    flex-direction: column;
    align-content: center;
    justify-content: center;
  }
  
  
  .card-content> img{
    width: 200px;
    max-width:80%;
    border-radius: 10px;
  }
  
  
  .card-content button{
    margin-top:40px;
    text-decoration: none;
    background-color: #ffff;
    color:#001e44 ;
    padding: 8px 12px;
    border-radius: 5px;
  }
  
  .card-content button:hover{ 
    background-color: #001e44;
    color: white;
  
  }
  
  .card-content button a{
     text-decoration: none;
  }
  
  #cDescription {
    color: white;
    font-family: "Lucida Console";
  }
  
  @media (max-width: 800px) and (min-width: 500px) {
    .details-button {
      display: block;
      
    .card-content button{ 
    display: none;
      }
	} 
  }
  
  @media (max-width: 800px) {
    .card {
      max-width: 500px;
    }
      .card-content button{
    display: none;
      }
    }
</style>
