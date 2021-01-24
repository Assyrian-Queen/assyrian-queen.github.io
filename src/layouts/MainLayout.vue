	ug<template lang="pug">
q-layout(view='lHh Lpr lFf')
	q-header(elevated)
		q-toolbar.q-pa-md
			q-btn(flat dense round icon='menu' aria-label='Menu' @click='leftDrawerOpen = !leftDrawerOpen')
			q-toolbar-title
				i.material-icons.md-36.q-mr-md rowing
				| Quietist Assyrians 

			div 
				i.material-icons.md-24.q-mr-md toys
				| Engenho Novo versão {{ $q.version }}
	q-drawer(v-model='leftDrawerOpen' show-if-above bordered content-class='bg-grey-1')
		q-list
			q-item-label.text-grey-8(header).

				Navegando Estes Vínculos

			EssentialLink(v-for='link in essentialLinks' :key='link.title' v-bind='link').


	q-page-container
		router-view.


</template>

<script>
import EssentialLink from 'components/EssentialLink.vue'

const linksData = [
						{
		title: 'Docs',
		caption: 'quasar.dev',
		icon: 'school',
		link: ''
	},
	{
		title: 'Github',
		caption: 'github.com/quasarframework',
		icon: 'code',
		link: ''
	},
	{
		title: 'Discord Chat Channel',
		caption: 'chat.quasar.dev',
		icon: 'chat',
		link: ''
	},
	{
		title: 'Forum',
		caption: 'forum.quasar.dev',
		icon: 'record_voice_over',
		link: ''
	},
	{
		title: 'Twitter',
		caption: '@quasarframework',
		icon: 'rss_feed',
		link: ''
	},
	{
		title: 'Facebook',
		caption: '@QuasarFramework',
		icon: 'public',
		link: ''
	},
	{
		title: 'Quasar Awesome',
		caption: 'Community Quasar projects',
		icon: 'favorite',
		link: ''
	}
];

export default {
	name: 'MainLayout',
	components: { EssentialLink },
	data () {
		return {
			leftDrawerOpen: false,
			essentialLinks: linksData
		}
	}
}
</script>
