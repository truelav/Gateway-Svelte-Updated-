<script>
	// import AOS from 'aos'
	// import 'aos/dist/aos.css'

	import seriesImageSrc1 from '../assets/Images/Home/product1.jpg'
	import seriesImageSrc2 from '../assets/Images/Home/product2.jpg'
	import LifestyleGallery from '../components/LifestyleGallery.svelte'
	import FeaturedProducts from '../components/FeaturedProducts.svelte'
	import FeaturesSeries from '../components/FeaturesSeries.svelte'

	// AOS.init();

</script>



	<!-- Top Section -->
	
	<section class="home-section-1" id="home-image-container-1">
		<div class="home-blob-container">
			<svg class="blob"
					data-aos="zoom-in-up"
					viewBox="0 0 600 600"
					xmlns="http://www.w3.org/2000/svg"
					>
					<g transform="translate(300,300)">
							<path d="M120,-157.6C152.7,-141.5,174.3,-102.6,194.8,-58.8C215.3,-14.9,234.6,33.8,228.4,80.8C222.2,127.8,190.4,173.1,148.1,184C105.8,195,52.9,171.5,-2.4,174.8C-57.8,178.2,-115.6,208.4,-137.5,190.9C-159.3,173.3,-145.3,108,-153,56.3C-160.7,4.6,-190.2,-33.4,-178.3,-54.2C-166.4,-75.1,-113.2,-78.8,-76.6,-93.6C-40,-108.3,-20,-134.2,11.9,-150.5C43.7,-166.8,87.4,-173.6,120,-157.6Z" fill="#def1fe" />
					</g>
			</svg>
		</div>
		<div class="home-content-container-1">
				<div class="">
						<div class="row">
								<div class="">
										<div class="md:container md:mx-auto home-info-container-1" 
										data-aos="fade-down-right"
										data-aos-offset="200"
										data-aos-delay="500"
										data-aos-duration="1000"
										data-aos-easing="ease-in-out"
										data-aos-mirror="true"
										data-aos-once="false">
												<h2 class="text-5xl">Welcome to</h2>
												<h1 class="text-8xl">Gateway</h1>
												<p class="mb-8 mt-8 leading-relaxed">
													Copper mug try-hard pitchfork pour-over freegan heirloom <br>
													neutra air plant cold-pressed tacos poke beard tote bag. <br>
													Heirloom echo park mlkshk tote bag selvage hot chicken <br>
													authentic tumeric truffaut hexagon try-hard chambray.
												</p>
												<button class="inline-flex text-white bg-indigo-500 border-0 py-2 px-6 focus:outline-none hover:bg-indigo-600 rounded text-lg">Buy Now</button>
										</div>
								</div>
						</div>
				</div>
		</div>
	</section>

	<!-- PARTNERS Section -->

	<section class="home-partners-section">
		<div class="home-partners-container">                    
				<div class="container flex m-auto">
						<div class="grid grid-cols-4 gap-4">
								<div class="flex">
										<img class="home-icon-image m-auto w-9/12" alt="microsoft" src="/images/Lifestyle/logo1.png"
										data-aos="fade-left"
										data-aos-delay="0"
										data-aos-duration="300"
										data-aos-easing="ease-in-out"
										data-aos-once="false">
								</div>
								<div class="flex">
										<img class="home-icon-image m-auto w-9/12" alt="windows 11" src="/images/Lifestyle/logo2.png"
										data-aos="fade-left"
										data-aos-delay="300"
										data-aos-duration="300"
										data-aos-easing="ease-in-out"
										data-aos-once="false">
								</div>
								<div class="flex">
										<img class="home-icon-image m-auto w-9/12" alt="miscrosoft 365" src="/images/Lifestyle/logo3.png"
										data-aos="fade-left"
										data-aos-delay="600"
										data-aos-duration="300"
										data-aos-easing="ease-in-out"
										data-aos-once="false">
								</div>
								<div class="flex">
										<img class="home-icon-image m-auto w-9/12" alt="gateway laptops" src="/images/Lifestyle/logo4.png"
										data-aos="fade-left"
										data-aos-delay="900"
										data-aos-duration="300"
										data-aos-easing="ease-in-out"
										data-aos-once="false">
								</div>
						</div>
				</div>
		</div>
	</section>

	<FeaturedProducts />

	<!-- <div class="home-3d-section">
		<iframe src='https://my.spline.design/gateway1-6d06b2b6fdc035bfc0c191cb695e6b26/' frameborder='0' width='100%' height='100%'></iframe>
	</div> -->

	<!-- Series Sections -->

	<section class="text-gray-600 body-font">
		<div class="container mx-auto flex px-5 py-24 md:flex-row flex-col items-center" >
			<div class="lg:max-w-lg md:w-1/2 lg:pr-24 md:pr-16 flex flex-col md:items-start md:text-left mb-16 md:mb-0 items-center text-center" 
			data-aos="fade-left"
			data-aos-delay="300"
			data-aos-duration="300"
			data-aos-easing="ease-in-out"
			data-aos-once="false">
				<h1 class="title-font sm:text-4xl text-3xl mb-4 font-medium text-gray-900">Before they sold out
					<br class="hidden lg:inline-block">readymade gluten
				</h1>
				<p class="mb-8 leading-relaxed">Copper mug try-hard pitchfork pour-over freegan heirloom neutra air plant cold-pressed tacos poke beard tote bag. Heirloom echo park mlkshk tote bag selvage hot chicken authentic tumeric truffaut hexagon try-hard chambray.</p>
				<div class="flex justify-center">
					<button class="inline-flex text-white bg-indigo-500 border-0 py-2 px-6 focus:outline-none hover:bg-indigo-600 rounded text-lg">Buy Now</button>
					<button class="ml-4 inline-flex text-gray-700 bg-gray-100 border-0 py-2 px-6 focus:outline-none hover:bg-gray-200 rounded text-lg">Learn More</button>
				</div>
			</div>
			<div class="lg:flex-grow lg:w-full md:w-2/3 w-5/6">
				<img class="object-cover object-center rounded" alt="hero" src={seriesImageSrc2} 
					data-aos="zoom-in"
					data-aos-delay="300"
					data-aos-duration="300"
					data-aos-easing="ease-in-out"
					data-aos-once="false">
			</div>
		</div>
	</section>

	<!-- Steps Section -->


	<section class="text-gray-600 body-font">
		<div class="container mx-auto flex px-5 py-24 md:flex-row flex-col items-center">
			<div class="lg:flex-grow lg:w-full md:w-1/2 w-5/6 mb-10 md:mb-0">
				<img class="object-cover object-center rounded" src={seriesImageSrc1} 
					alt="hero" 
					data-aos="zoom-in"
					data-aos-delay="300"
					data-aos-duration="300"
					data-aos-easing="ease-in-out"
					data-aos-once="false">
			</div>
			<div  class="lg:max-w-lg md:w-1/2 lg:pl-24 md:pl-16 flex flex-col md:items-start md:text-left items-center text-center" 	
					data-aos="fade-down-left"
					data-aos-delay="0"
					data-aos-duration="600"
					data-aos-easing="ease-in-out"
					data-aos-once="false">
				<h1 class="title-font sm:text-4xl text-3xl mb-4 font-medium text-gray-900">Before they sold out
					<br class="hidden lg:inline-block">readymade gluten
				</h1>
				<p class="mb-8 leading-relaxed">Copper mug try-hard pitchfork pour-over freegan heirloom neutra air plant cold-pressed tacos poke beard tote bag. Heirloom echo park mlkshk tote bag selvage hot chicken authentic tumeric truffaut hexagon try-hard chambray.</p>
				<p class="mb-8 leading-relaxed">Copper mug try-hard pitchfork pour-over freegan heirloom neutra air plant cold-pressed tacos poke beard tote bag. Heirloom echo park mlkshk tote bag selvage hot chicken authentic tumeric truffaut hexagon try-hard chambray.</p>
				<div class="flex justify-center">
					<button class="inline-flex text-white bg-indigo-500 border-0 py-2 px-6 focus:outline-none hover:bg-indigo-600 rounded text-lg">Buy Now</button>
					<button class="ml-4 inline-flex text-gray-700 bg-gray-100 border-0 py-2 px-6 focus:outline-none hover:bg-gray-200 rounded text-lg">Learn Now</button>
				</div>
			</div>
		</div>
	</section>

  <!-- Features Sections -->
	<FeaturesSeries />

	<!-- Gallery Section -->

	<LifestyleGallery />

	<!-- Bottom Text Container -->

	<section class="text-gray-600 body-font">
		<div class="container px-5 py-24 mx-auto flex flex-wrap">
			<h2 class="sm:text-3xl text-2xl text-gray-900 font-medium title-font mb-2 md:w-2/5">Kickstarter Actually Pinterest Brunch Bitters Occupy</h2>
			<div class="md:w-3/5 md:pl-6">
				<p class="leading-relaxed text-base">Taxidermy bushwick celiac master cleanse microdosing seitan. Fashion axe four dollar toast truffaut, direct trade kombucha brunch williamsburg keffiyeh gastropub tousled squid meh taiyaki drinking vinegar tacos.</p>
				<div class="flex md:mt-4 mt-6">
					<button class="inline-flex text-white bg-indigo-500 border-0 py-1 px-4 focus:outline-none hover:bg-indigo-600 rounded">Button</button>
					<a class="text-indigo-500 inline-flex items-center ml-4" href="/">Learn More
						<svg fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" class="w-4 h-4 ml-2" viewBox="0 0 24 24">
							<path d="M5 12h14M12 5l7 7-7 7"></path>
						</svg>
					</a>
				</div>
			</div>
		</div>
	</section>
		


<style>
	.home-3d-section{
		height: 80vh;
	}
</style>