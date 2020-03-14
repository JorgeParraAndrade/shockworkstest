<template>
	<nav class="main-navigation">
		<div class="main-logo">
			<img src="../assets/img/logo.png" alt="shockworks" />
		</div>
		<div class="menu-container">
			<ul class="menu-list">
				<li class="menu-item"><a href="#" class="active">Home </a></li>
				<li class="menu-item"><a href="#">About </a></li>
				<li class="menu-item"><a href="#">Portfolio </a></li>
				<li class="menu-item"><a href="#">Product </a></li>
				<li class="menu-item"><a href="#">Career </a></li>
				<li class="menu-item"><a href="#">Blog </a></li>
			</ul>
			<input type="text" class="search-box" />
			<a href="#" class="btn-main">Contact Us</a>
		</div>
	</nav>
</template>

<script>
export default {}
</script>

<style lang="scss">
.main-navigation {
	display: flex;
	flex-direction: row;
	justify-content: space-between;
	align-items: center;
	padding: 60px;

	.main-logo {
		width: 300px;

		img {
			width: 100%;
		}
	}

	.menu-container {
		display: flex;
		flex-direction: row;
		justify-content: center;
		align-items: center;

		.menu-list {
			list-style: none;
			display: flex;
			flex-direction: row;
			justify-content: center;
			align-items: center;
			margin: 0 30px;

			.menu-item {
				font-size: 17px;
				color: #555555;
				padding: 20px;

				a {
					color: inherit;
					text-decoration: none;
					position: relative;

					&:hover {
						color: #185f7f;
					}

					&.active {
						color: #185f7f;
						&:after {
							content: '';
							width: 8px;
							height: 8px;
							background-color: #185f7f;
							position: absolute;
							border-radius: 50px;
							bottom: -15px;
							left: calc(50% - 4px);
						}
					}
				}
			}
		}

		.search-box {
			border: solid 2px #c6baf8;
			border-radius: 4px;
			height: 50px;
			width: 350px;
			background-image: url('../assets/img/mglass.png');
			background-repeat: no-repeat;
			background-position: 97%;
			margin: 0 40px 0 0;
			padding: 10px 45px 10px 10px;
		}
	}
}
</style>
