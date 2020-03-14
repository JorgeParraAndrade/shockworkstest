<template>
	<div>
		<Header />
		<div class="container">
			<div class="col-container">
				<div class="col-40">
					<h2>The Process About Our Work</h2>
					<p>
						<span>Alejandro Laplana</span> leads and adaptable end-to-end
						development team consisting of a large portion of captable
						enterprise mixed reality solutions.
					</p>
					<a href="#" class="btn-main-outline">Know More</a>
				</div>
				<div class="col-60">
					<div class="image-container" :style="{ 'backgroundImage': `url(${Image1})`}" >
						<img src="../assets/img/comp4.png" alt="city" />
					</div>
				</div>
			</div>
			<div class="col-container">
				<div class="col-60">
					<div class="image-container" :style="{ 'backgroundImage': `url(${Image1})`}" >
						<img src="../assets/img/comp3.png" alt="city" />
					</div>
				</div>
				<div class="col-40">
					<h2>We are here to <b>always help</b> you</h2>
					<p>
						<span>Alejandro Laplana</span> leads and adaptable end-to-end
						development team consisting of a large portion of captable
						enterprise mixed reality solutions.
					</p>
					<a href="#" class="btn-main-outline">Know More</a>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
import Header from '../components/Header'
import Image1 from '~/assets/img/back3.png'
export default {
	data() {
    return { Image1 }
  },
	components: {
		Header
	}
}
</script>

<style lang="scss">
.container {
	max-width: 80%;
	margin: 0 auto;
}

.col-container {
	display: flex;
	justify-content: center;
	align-items: center;

	.col-40 {
		width: 40%;
	}

	.col-50 {
		width: 50%;
	}

	.col-60 {
		width: 60%;
	}
}

.image-container{
	background-size: contain;
	background-position: center;
	background-repeat: no-repeat;
	width: 100%;
}
</style>
