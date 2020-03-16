<template>
	<section class="header">
		<div class="main-image">
			<div class="center-container">
				<img src="../assets/img/component.png" alt="work" />
				<h1>
					A brand new day to see the world
				</h1>
				<div class="btn-container">
					<a href="#" class="btn-main">Our Works</a>
					<a href="#" class="btn-main-outline">Know More</a>
				</div>
			</div>
		</div>
	</section>
</template>

<style lang="scss" scoped>
.header {
	width: 100%;
	height: calc(100vh - 203px);
	display: flex;
	flex-direction: column;
	align-items: center;
	justify-content: center;
	background-image: url('../assets/img/back1.png');
	background-size: cover;

	.main-image {
		.center-container {
			margin: 20px 0;
			img {
				@media (max-width: 768px) {
					width: 100%;
				}
			}
			h1 {
				font-size: 50px;
				color: #222222;
				max-width: 480px;
				margin: 0 auto;
				text-transform: capitalize;
				line-height: 1.2;
				text-align: center;

				@media (max-width: 768px) {
					font-size: 35px;
					margin: 30px 0;
				}
			}
			.btn-container {
				display: flex;
				flex-direction: row;
				align-items: center;
				justify-content: space-evenly;
				max-width: 440px;
				margin: 25px auto;
			}
		}
	}
}
</style>
