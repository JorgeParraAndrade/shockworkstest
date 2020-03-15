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

		<section class="specialty">
			<h3><span>What is the</span> Speciality Of Us?</h3>
			<div v-swiper:mySwiper="swiperOption">
				<div class="swiper-wrapper">
						<div class="swiper-slide" v-for="banner in serverData.articles" :key="banner.id">
							<div class="card-image-container">
								<img :src="banner.urlToImage">
							</div>
							<h4>{{ banner.title.substring(0, 12) + '...' }}</h4>
							<p>{{ banner.description }}</p>
						</div>
				</div>
				<div class="navigation-arrow">
					<button class="btn-slider" @click="mySwiper.slidePrev()"><img src="../assets/img/larrow.png" alt=""></button>
					<button class="btn-slider" @click="mySwiper.slideNext()"><img src="../assets/img/rarrow.png" alt=""></button>
				</div>
			</div>
		</section>


		<div class="container">
			<div class="partners-section">
				<h3>Our Partnes & Clients</h3>
				<div class="card-deck">
					<div class="client-card">
						<img src="../assets/img/logo1.png" alt="client">
						<a href="#">Learn More</a>
					</div>
					<div class="client-card">
						<img src="../assets/img/logo2.png" alt="client">
						<a href="#">Learn More</a>
					</div>
					<div class="client-card">
						<img src="../assets/img/logo3.png" alt="client">
						<a href="#">Learn More</a>
					</div>
					<div class="client-card">
						<img src="../assets/img/logo4.png" alt="client">
						<a href="#">Learn More</a>
					</div>
					<div class="client-card">
						<img src="../assets/img/logo5.png" alt="client">
						<a href="#">Learn More</a>
					</div>
					<div class="client-card">
						<img src="../assets/img/k.png" alt="client">
						<a href="#">Learn More</a>
					</div>
				</div>
			</div>
		</div>

	</div>
</template>

<script>
import Header from '../components/Header'
import Image1 from '~/assets/img/back3.png'
import Image2 from '../assets/img/pic1.png'
import Image3 from '../assets/img/pic2.png'
import Image4 from '../assets/img/pic3.png'
export default {
	async asyncData({ $axios }) {
		try{
			let serverData = await $axios.$get(`http://newsapi.org/v2/top-headlines?country=us&apiKey=bdca2dcef4ca4fb2af7374dffc557c4d`);
			return { serverData }
		}
		catch(error){
			console.log(error);
		}
	},
	data() {
    return {
			Image1,
			swiperOption: {
				loop: true,
				slidesPerView: 5,
				centeredSlides: true,
				spaceBetween: 35,
				watchSlidesProgress: true,
				watchSlidesVisibility: true,
				slideVisibleClass: 'active',
				on: {
					imagesReady() {
						document.querySelectorAll('.active').forEach(a => a.classList.remove('blur'));
						this.visibleSlides[0].classList.add('blur')
						this.visibleSlides[this.visibleSlides.length-1].classList.add('blur')
					},
					slideChange() {
						document.querySelectorAll('.active').forEach(a => a.classList.remove('blur'));
						this.visibleSlides[0].classList.add('blur')
						this.visibleSlides[this.visibleSlides.length-1].classList.add('blur')
					}
				}
			}	
		}
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

.image-container {
	background-size: contain;
	background-position: center;
	background-repeat: no-repeat;
	width: 100%;
}

.partners-section {

	h3{
		text-align: center;
    font-size: 45px;
    margin-top: 70px;
    font-family: montserrat;
	}

	.card-deck {
		display: flex;
		align-items: center;
		justify-content: center;
		flex-wrap: wrap;

		.client-card {
			width: 30%;
			background-color: white;
			padding: 0;
			min-height: 360px;
			border-radius: 5px;
			margin: 20px;
			display: flex;
			align-items: center;
			justify-content: space-evenly;
			flex-direction: column;
			box-shadow: 0px 10px 30px #99999933;

			&:nth-child(1) {
				margin-top: 120px;
			}	
			&:nth-child(3) {
				margin-top: 120px;
			}	
			&:nth-child(5) {
				margin-top: -80px;
			}	

			&:hover {
				background-color: #185f7f;

				a {
					color: #fff;
					transform: translateY(5px) scale(1.1);
				}

				img {
					filter: brightness(0) invert(1);
				}
			}

			a {
				color: #185f7f;
				text-decoration: none;
				font-weight: 500;
				transition: all ease 0.3s;
			}

			img {
				max-width: 100%;
			}
		}
	}
}

.specialty {
	h3{
		text-align: center;
    font-size: 45px;
    margin-top: 70px;
    margin-bottom: 70px;
    margin-left: auto;
    margin-right: auto;
    font-family: montserrat;
		max-width: 400px;

		span{
			font-weight: 400;
		}
	}
}

.swiper-container {
	width: 100%;

	.active{
		&.blur{
			transform: scale(0.9);

			img {
				filter: blur(3px);
			}
		}

	}
	

	.swiper-slide {
		text-align: center;
		font-size: 38px;
		font-weight: 700;
		background-color: rgb(255, 255, 255);
		display: flex;
		justify-content: center;
		align-items: center;
		flex-direction: column;
		transition: all ease 0.4s;
		box-shadow: 0px 10px 30px #99999933;
		padding: 25px 40px;

		h4 {
			font-size: 24px;
			font-family: poppins;
			margin: 20px 0;
			color: #222222;
		}

		p {
			font-size: 13px;
			color: #555555;
			text-align: center;
			font-family: poppins;
			font-weight: 400;
			margin: 0 0 40px;
			max-height: 50px;
    	overflow-y: hidden;
		}

	}
	.swiper-pagination {
		> .swiper-pagination-bullet {
			background-color: red;
		}
	}
}

.navigation-arrow{
	text-align: center;
	margin: 25px 0;
}

.card-image-container {
	height: 200px;
	width: 200px;
	border-radius: 600px;
	overflow: hidden;
	display: flex;
	align-items: center;
	justify-content: center;

	img {
		height: 100%;
	}
}

.btn-slider{
	padding: 15px 17px;
	background-color: white;
	border: none;
	border-radius: 50px;
	box-shadow: 0px 10px 30px #99999933;
	cursor: pointer;

	img {
		max-width: 15px;
	}
}

</style>
