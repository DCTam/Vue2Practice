<template>
    <div class="container">
		<app-header :quoteCount="quotes.length" :maxQuotes="maxQuotes"></app-header>
		<app-new-quote @quoteAdded="newQuote($event)"></app-new-quote>
		<app-quote-grid @deleteQuote="deleteQuote($event)" :quotes="quotes"></app-quote-grid>

		<div class="row">
			<div class="col-sm-12 text-center">
				<div class="alert alert-info">Info: Click on a Quote to delete it!</div>
			</div>
		</div>
    </div>
</template>

<script>
	import QuoteGrid from './components/grid.vue';
	import NewQuote from './components/new_quote.vue';
	import Header from './components/header.vue';

    export default {
        data: function (){
			return {
				quotes: [
					'First quote'
				],
				maxQuotes: 10
			}
		},
		components: {
			appQuoteGrid: QuoteGrid,
			appNewQuote: NewQuote,
			appHeader: Header
		},
		methods: {
			newQuote(quote){
				if(this.quotes.length >= this.maxQuotes){
					alert("Please delete some quotes first");
					return;
				}
				this.quotes.push(quote);
			},
			deleteQuote(index){
				this.quotes.splice(index, 1);
			}
		}
    }
</script>

<style>
</style>
