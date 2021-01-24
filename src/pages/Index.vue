<template lang="pug">
q-page.flex.flex-center
	#bg
		img(src="../assets/images/nyc-dynamo.jpg" style="filter: contrast(40%);")
	.hero-text
		img(alt='Laser Phaser' src='~assets/images/biohazard-white.svg' width="125px")
		h4.q-mb-sm.q-mt-md Active Galactic Nuclei
			h5.q-my-md Some Quasars Are Quite, Quite Far
		.fit.row.q-gutter-md.justify-center
			q-btn(label='Rashidun' color='primary' @click='fullHeight = true')
			q-btn.q-ml-md(color="secondary") Astronomy
			q-btn.q-ml-md(color="negative") Astrology


		q-dialog(v-model='fullHeight' full-height)
			q-card.column.full-height(style="width: 300px;")
				q-img(src='../assets/images/nyc-more-chrysler.jpg')
					.absolute-bottom
						.text-h6 Lofty Modernism
						.text-subtitle2 Gotham Skyline
				q-card-actions
					q-btn(color="secondary" @click='fullHeight = false') Tigris
					q-btn(color="negative" @click='fullHeight = false') Euphrates

</template>

<script>
export default {
	data () {
		return {
			small: false,
			medium: false,
			fullWidth: false,
			fullHeight: false
		}
	}
}
</script>




//- q-page.flex.flex-center.fill-height
//- 	img(alt='Biohazard Quanantine' src='~assets/images/biohazard.svg' width="250px")
//- 	.fit.row.wrap.justify-center.items-start
//- 		q-btn.q-mr-lg(round color="negative" size="xl")
//- 			i.material-icons.md-48 all_inclusive
//- 		q-btn.q-mr-lg(round color="primary" size="xl")
//- 			i.material-icons.md-48 smoking_rooms
//- 		q-btn(round color="positive" size="xl")
//- 			i.material-icons.md-48 autorenew

</template>

<script>
export default {
	name: 'PageIndex'
}
</script>
