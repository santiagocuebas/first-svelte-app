<script>
	export let image;
	export let fullname;
	export let country;
	export let work;
	export let company;
	export let testimony;
</script>

<div class='container-testimony'>
	<img
		class='img-testimony'
		src={`./images/testimony-${image}.png`}
		alt={`Photo of ${image}`}
	/>
	<div class='container-text-testimony'>
		<p class='name-testimony'><strong>{fullname}</strong> in {country}</p>
		<p class='work-testimony'>{work} at <strong>{company}</strong></p>
		<p class='content-testimony'>"{@html testimony}"</p>
	</div>
</div>

<style>
	.container-testimony {
		display: flex;
		align-items: center;
		width: fit-content;
		height: min-content;
		background-color: #fff;
		box-shadow: 0 3px 13px 1px #ccc;
	}
	
	.img-testimony {
		width: 350px;
		height: 350px;
	}
	
	.container-text-testimony {
		min-width: 550px;
		width: 100%;
		max-width: 750px;
		height: 350px;
		text-align: center;
		padding: 40px;
		line-height: 1.5rem;
		font-family: Lato, sans-serif;
		font-weight: 400;
		color: #444;
	}
	
	.name-testimony, .work-testimony, .content-testimony {
		font-size: 1.3rem;
		margin: 15px;
	}
	
	.content-testimony {
		font-size: 1.1rem;
		text-align: justify;
	}
</style>
