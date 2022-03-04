<script>
	import router from "page"
	import Home from './routes/Home.svelte'
	import AllProducts from './routes/AllProducts.svelte'
	import Product from './routes/Product.svelte'
	import About from './routes/About.svelte'
	import Contact from './routes/Contact.svelte'
	import Support from "./routes/Support.svelte"
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
	router('/Windows11', () => (page = Windows11))
	router('/Product/:id',
		(ctx, next) => {
			params = ctx.params
			next()
		}, 
		() => page = Product
	)

	router.start()
</script>


	<TailwindCss />

	<Header />

	<main>
		<svelte:component this="{page}" params="{params}" />
	</main>

	<Footer />


<style>
</style>
