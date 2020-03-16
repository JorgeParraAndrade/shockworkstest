<template>
	<div>
		<main-menu />
		<nuxt />
	</div>
</template>

<script>
import MainMenu from '../components/MainMenu'
export default {
	components: {
		MainMenu
	}
}
</script>

<style lang="scss">
html {
	font-family: 'Poppins', sans-serif;
	font-size: 16px;
	word-spacing: 1px;
	-ms-text-size-adjust: 100%;
	-webkit-text-size-adjust: 100%;
	-moz-osx-font-smoothing: grayscale;
	-webkit-font-smoothing: antialiased;
	box-sizing: border-box;
}

*,
*:before,
*:after {
	box-sizing: border-box;
	margin: 0;
}

h2 {
	font-size: 45px;
	font-family: 'Montserrat';
	font-weight: 400;
	max-width: 390px;
}

p {
	color: #555555;
	line-height: 27px;
	margin: 40px 0 40px;

	span {
		font-weight: 500;
	}
}

.button--green {
	display: inline-block;
	border-radius: 4px;
	border: 1px solid #3b8070;
	color: #3b8070;
	text-decoration: none;
	padding: 10px 30px;
}

.btn-main {
	width: 169px;
	height: 58px;
	background: transparent linear-gradient(248deg, #1b92c8 0%, #2c3636 100%) 0%
		0% no-repeat padding-box;
	opacity: 1;
	border-radius: 4px;
	border: solid 1px linear-gradient(248deg, #1b92c8 0%, #2c3636 100%);
	color: #ffffff;
	text-decoration: none;
	display: flex;
	align-items: center;
	justify-content: center;
	cursor: pointer;
}

.btn-main-outline {
	width: 169px;
	height: 58px;
	background: transparent;
	border: solid 1px #185f7f;
	opacity: 1;
	border-radius: 4px;
	color: #185f7f;
	text-decoration: none;
	display: flex;
	align-items: center;
	justify-content: center;
	transition: all ease 0.3s;
	cursor: pointer;

	&:hover {
		color: #fff;
		border: 1px solid transparent;
		background: transparent linear-gradient(248deg, #1b92c8 0%, #2c3636 100%) 0%
			0% no-repeat padding-box;
	}
}
</style>
