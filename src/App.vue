<template>
	<div :id="$style.app">
		<ApartmentsItem 
			:descr="apartment.description"
			:price="apartment.price"
			:rating="apartment.rating"
			:imgSrc="apartment.photo"
		/>
	</div>
</template> 

<script>
import ApartmentsItem from './components/apartment/ApartmentsItem.vue';
export default {
	name: 'App',
	components: {
		ApartmentsItem
	},
	data() {
		return {
			apartment: {
				description: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Illo nobis quasi cupiditate hic soluta laborum corporis est velit sit animi?',
				photo: 'https://cdn.pixabay.com/photo/2015/04/23/22/00/tree-736885__340.jpg',
				price: 1200,
				rating: 4.3
			}
		}
	}
}
</script>

<style module>
#app {
  font-family: Montserrat, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.btn {
	background-color: #f46666;
	color: #fff;
	&--outlined {
		border: 5px solid #1f61a3;
	}
}
</style>

