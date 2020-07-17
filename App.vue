<script>
	export default {
		onLaunch: function() {
			console.log('App Launch')
		},
		onShow: function() {
			console.log('App Show')
		},
		onHide: function() {
			console.log('App Hide')
		}
	}
</script>

<style>
	/*每个页面公共css */
	* {
	  margin: 0;
	  padding: 0;
	}
	a {
	  text-decoration: inherit;
	}
	ul,
	ol {
	  list-style: none;
	}
	h1,
	h2,
	h3,
	h4 {
	  font: inherit;
	}
	input,
	select,
	button {
	  font: inherit;
	}
	html,
	body {
	  height: 100%;
	  -webkit-user-select: none;
	  -webkit-touch-callout: none;
	  -webkit-tap-highlight-color: transparent;
	}
	body {
	  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen,
	    Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
	}
	#app {
	  height: 100%;
	  overflow: hidden;
	}
</style>
