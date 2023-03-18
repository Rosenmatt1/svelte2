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

	$: count = feedback.length
	$: average = feedback.reduce((a, {rating}) => 0) / count 

	const deleteFeedback = (e) => {
		const itemId = e.detail
		feedback = feedback.filter((item) =>item.id != itemId)
	}
</script>

<!-- if passing a prop that is named the same, don't need to name it -->
<main class="container">
	<FeedbackList {feedback} on:delete-feedback={deleteFeedback}/>
</main>

