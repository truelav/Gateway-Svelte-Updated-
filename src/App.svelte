<script>
	import router from "page"
	import AOS from 'aos'
	import 'aos/dist/aos.css'

	import Home from './routes/Home.svelte'
	import AllProducts from './routes/AllProducts.svelte'
	import Product from './routes/Product.svelte'
	import About from './routes/About.svelte'
	import Contact from './routes/Contact.svelte'
	import Support from "./routes/Support.svelte"
	import Recycle from "./routes/Recycle.svelte"
	import Windows11 from "./routes/Windows11.svelte"

  import Header from './components/Header.svelte'
  import Footer from './components/Footer.svelte'

	import TailwindCss from './TailwindCSS.svelte'
  import './TailwindCSS.css'

  let page
	let params

	router('/', () => (page = Home))
	router('/AllProducts', () => (page = AllProducts))
	router('/About', () => (page = About))
	router('/Contact', () => (page = Contact))
	router('/Support', () => (page = Support))
	router('/Recycle', () => (page = Recycle))
	router('/Windows11', () => (page = Windows11))
	router('/Product/:id',
		(ctx, next) => {
			params = ctx.params
			next()
		}, 
		() => page = Product
	)

	router.start()

	AOS.init({
		// Settings that can be overridden on per-element basis, by `data-aos-*` attributes:
		offset: 150, // offset (in px) from the original trigger point
		delay: 300, // values from 0 to 3000, with step 50ms
		duration: 300, // values from 0 to 3000, with step 50ms
		once: false, // whether animation should happen only once - while scrolling down
		mirror: false, // whether elements should animate out while scrolling past them
		anchorPlacement: 'top-bottom', // defines which position of the element regarding to window should trigger the animation
	});
</script>


	<TailwindCss />

	<Header />

	<main>
		<svelte:component this="{page}" params="{params}" />
	</main>

	<Footer />


<style>
</style>
