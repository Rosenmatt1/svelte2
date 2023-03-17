<script>
	import FeedbackList from './components/FeedbackList.svelte'

	let feedback = [
		{
			id: 1,
		rating: 10,
		text: "Lorem Ipsum was the best I have ever tasted"
		},
		{
			id: 2,
		rating: 8,
		text: "Overall it was good.  A bit pricey"
		},
		{
			id: 3,
		rating: 3,
		text: "The worst around"
		}
	]
</script>

<!-- if passing a prop that is named the same, don't need to name it -->
<main>
	<FeedbackList {feedback}/>
</main>

