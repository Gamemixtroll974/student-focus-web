<script lang="ts">
</script>

<nav class="nav">
	<div class="left-items">
		<div class="title">
			<h1>Student Focus</h1>
		</div>
	</div>
	<div class="center-items">
		<a href="/">Accueil</a>
		<a href="/notes">Notes</a>
	</div>
</nav>

<style lang="scss">
	@import url('https://fonts.googleapis.com/css2?family=Poppins&display=swap');
	:root {
		--poppins: 'Poppins', sans-serif;
	}

	.nav {
		display: flex;
		justify-content: space-between;
		align-items: center;
		background-color: #272727;
		color: #fff;
		height: 56px;

		.left-items {
			flex: 1;
			.title {
				h1 {
					margin: 0;
					margin-left: 10px;
					font-family: var(--poppins);
					letter-spacing: 0.5px;
					text-decoration: underline;
				}
			}
		}

		.center-items {
			flex: 1;

			a {
				color: #fff;
				position: relative;
				text-decoration: none;
				font-family: var(--poppins);
				margin-right: 10px;

				&::before {
					content: '';
					position: absolute;
					width: 100%;
					height: 4px;
					background-color: #ffffff;
					border-radius: 5px;
					bottom: 0;
					transform: scaleX(0);
					transition: transform 0.3s ease-in-out;
				}

				&:hover::before {
					transform: scaleX(1);
				}
			}
		}
	}
</style>
