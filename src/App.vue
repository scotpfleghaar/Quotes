<template>
    <div class="container">
        <app-new-quote @quoteAdded="newQuote"></app-new-quote>
        <app-quote-grid :quotes="quotes" @quoteDeleted="deleteQuote"></app-quote-grid>
        <div class="row">
            <div class="col-sm-12 text-center">
                <div class="alert alert-info">Info: Click on a quote to delete it</div>
            </div>
        </div>
    </div>
</template>

<script>
import quoteGrid from "./components/QuoteGrid.vue";
import newQuote from "./components/NewQuote.vue";
export default {
    data: function(){
        return {
            quotes: [
                "Just a quote"
            ],
            maxQuotes: 10,
        }
    },
    components: {
        appQuoteGrid: quoteGrid,
        appNewQuote: newQuote,
    },
     methods: {
         newQuote(quote){
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
