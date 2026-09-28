<script>
import '@fontsource/ibm-plex-mono/400.css';
  import '@fontsource/ibm-plex-mono/500.css';
  import '@fontsource/ibm-plex-mono/700.css';
	let name = $state('world');
	let curr = $state(1);
	function set(i) {
		curr = i;
	}

	import { ArrowUpRight } from 'lucide-svelte';

	const links = [
		{
			label: 'Spring Nectar Recital',
			url: 'https://www.springnectaracademy.org/events--tours.html'
		},
		{
			label: 'LinkedIn',
			url: 'https://www.linkedin.com/in/yashvasin-hariharan-799392344/'
		},
		{
			label: 'Email',
			url: 'mailto:yashvasin76@gmail.com'
		}
	];
</script>

<header class="top-bar">
	<h1 onclick={() => set(1)}>about me</h1>
	<h1 onclick={() => set(2)}> EC's </h1>
	<h1 onclick={() => set(3)}> academics </h1>
	<h1 onclick={() => set(4)}> socials</h1>
	<h1 onclick={() => set(5)}> pictures </h1>
</header>


<main> 
{#if curr === 1}
<div> 
	<h1> About Me </h1>
<p>I am a current 10th grader at Whitney Gretchen High School. As of now, I am most interested in majoring in Computer Science, with a focus on AIML and neural networks, as I feel this will expand new frontiers as we can identify patterns and solve problems in a natural, adaptable way, rather than using traditional algorithms.
</p>

<p>
	I grew up surrounded by Indian cultural and am very much in touch with my ancestral roots. I am proficient in Tamil and I am Carnatic vocalist. My parents frequent temples, and there I learn reverence and patience. 
</p>
	<h2> Traits </h2>
	<p>
	If I set my mind to something, I am mostly hardworking and despise lackluster work. One of my main flaws would be my forgetfulness, and lack of organization.
	</p>
</div>

{:else if curr === 2}
<div> 
	<h1> Extracurriculars </h1>

	<ul>
	  <li>Earned the Sangeetha Yuvagayaka title in Carnatic Vocal Singing at Spring Nectar Academy.</li>
	  <li>In WHS, serving as the Tech Chair for the CyberPatriots Club.</li>
	  <li>Completed AP Computer Science A (APCSA) with a top score of 5.</li>
	  <li>Competed in numerous hackathons, frequently winning awards in collegiate-level environments.</li>
	  <li>Holds the Life Scout rank with over 50 hours of hands-on community service.</li>
	</ul>
</div>

{:else if curr === 3}
<div>
			<h1>Academics</h1>
			<p>
				I am at Whitney Gretchen High School, the number 1 school in California. 
				Currently, I am self-studying AP Physics, and am taking AP Human Geo as well as AP Stats in school.
			</p>
			<p>
				I am taking USACO and ASAIO, and currently have a 5.0 GPA.
			</p>
		</div>

{:else if curr === 4}
	<h1> Socials and References </h1>
	<ul class="link-list">
	{#each links as link}
		<li>
			<a href={link.url} class = "underline" >
				<span>{link.label}</span>
				<ArrowUpRight class="icon" size={18} />
			</a>
		</li>
	{/each}
</ul>
{:else if curr == 5} 
<h1> Picture </h1> 
<img src="https://images.chesscomfiles.com/uploads/v1/user/81012526.90bad6d0.200x200o.71052a7b768a.jpeg/> 
<img src="https://www.springnectaracademy.org/uploads/1/7/2/9/17292304/01-0289-09242023-2_orig.jpg"/>
{/if}
</main>




<style>

	:global(*) {
		box-sizing: border-box;
		margin: 0;
		padding: 0;
    
	}
:global(html),
:global(body),
:global(#app) {
  margin: 0;
  padding: 0;
  min-height: 100vh;
  background-color: #282828 !important;
  color: #ebdbb2;
  font-family: 'IBM Plex Mono', monospace
}

	.top-bar {
		position: sticky;
		top: 0;
		display: flex;
		justify-content: space-between;
		align-items: center;
		background-color: #1d2021;
		color: #ffffff;
		padding: 0.8rem 2rem;
		height: 3rem
	}

	.top-bar h1 {
		font-size: 1rem; 
		font-weight: 500; 
		color: #fb4934;
		line-height: 1;
		margin: 0;
    cursor: pointer; 
    user-select: none;
    transition: transform 0.2s ease-in-out, color, 0.2s ease-in-out
	}
  .top-bar h1:hover { 
    transform: scale(1.1);
    color: #f86e5f
  }
main {
		padding: 2rem;
		max-width: 800px;
		margin: 0 auto;
	}

	h1 {
		font-size: 1.6rem;
		color: #fabd2f; 
		margin-bottom: 1.25rem;
	}

	h2 {
		font-size: 1.25rem;
		color: #83a598; 
		margin-top: 1.75rem;
		margin-bottom: 0.75rem;
	}

	p {
		margin-bottom: 1.25rem;
		line-height: 1.65;
		color: #ebdbb2;
	}
	ul {
		padding-left: 2rem;
	}
.link-list {
	list-style: none
}
.link-list a {
  display: inline-flex;
  align-items: center;
  gap: 0.35rem;
  color: #83a598; 
  font-weight: 500;
  text-decoration: underline 2px rgba(250, 189, 47, 0);
  

  transition: color 0.2s ease, text-decoration-color 0.3s ease;
}

.link-list a:hover {
  color: #fabd2f; 

  text-decoration-color: rgba(250, 189, 47, 1);
}



	.link-list a:hover {
		color: #fabd2f; 
		text-decoration-color: rgba(0, 123, 255, 1)
	}

	:global(.icon) {
		display: inline-block;
		vertical-align: middle;
	}
	</style>
