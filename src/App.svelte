<script>
	import FeedbackList from './components/FeedbackList.svelte'

	let feedback = [
		{
			id: 1,
			rating: 10,
			text: 'Lorem ipsum ai queas dela monzah dekiu aoi c oaiw oia woa oc vseda cawdawfvsv dwafsvsfe fawdaw eawad/'
		},
		{
			id: 2,
			rating: 9,
			text: 'Lorem ipsum ai queas dela monzah dekiu aoi c oaiw oia woa oc vseda cawdawfvsv dwafsvsfe fawdaw eawad/'
		},
		{
			id: 3,
			rating: 8,
			text: 'Lorem ipsum ai queas dela monzah dekiu aoi c oaiw oia woa oc vseda cawdawfvsv dwafsvsfe fawdaw eawad/'
		}

	]

	const deleteFeedback = (e) => {
		const itemId = e.detail
		feedback = feedback.filter((item) => item.id != itemId)
	}
</script>

<main class="container">
	<FeedbackList {feedback} on:delete-feedback={deleteFeedback}/>
</main>