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
</style>
