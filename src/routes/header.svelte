<script lang="ts">

	import * as config from '$lib/config'
</script>


<nav>
	<div class="logo-title-container">
		<img src="pvp-acm.png" alt="acm-pvp-logo" class="logo" height="15%" width="15%">
		<a href="/" class="title">
			<b>{config.title}</b>
		</a>
	</div>
	<ul class="links">
		<li >
			<a href="/events">Events</a>
		</li>
		<li>
			<a href="/gallery">Gallery</a>
		</li>
		<li>
			<a href="/members">Members</a>
		</li>
		<li>
			<a href="/about-us">About Us</a>
		</li>
	</ul>
</nav>
<style>
	nav {
		padding-block: var(--size-7);
	}

	.logo-title-container {
		display: flex;
		align-items: center;
	}

	.logo {
		margin-right: var(--size-7); /* Adjust the margin as needed */
	}
	.links {
		margin-block: var(--size-7);
	}

	a {
		color: inherit;
		text-decoration: none;
		padding: 10px;
	}

	@media (min-width: 768px) {
		nav {
			display: flex;
			justify-content: space-between;
		}

		.links {
			display: flex;
			gap: var(--size-7);
			margin-block: 0;
		}
	}
	.links a:hover {
	  position: relative;
    }
	.links a:hover::after {
      content: '';
      display: block;
      width: 100%;
      height: 3px; /* Adjust the thickness of the underline */
      background-color: #3498db; /* Underline color */
      position: absolute;
      bottom: 0;
      left: 0;
      transition: width 0.3s ease; /* Add a smooth transition effect */
    }
    /* Apply underline to elements with a specific class on hover */
    .links .underline-text:hover {
      text-decoration: underline;
    }
	.links .underline-text:hover::after {
      content: '';
      display: block;
      width: 100%;
      height: 5px; /* Adjust the thickness of the underline */
      background-color: #e74c3c; /* Underline color */
      position: absolute;
      bottom: 0;
      left: 0;
      transition: width 0.3s ease; /* Add a smooth transition effect */
    }

</style>
