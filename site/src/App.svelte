<script>
	import { 
		Theme,
		Select,
		Card,
		TextArea,
		Button,
		Input,
		// Text,
		// SmallText,
		SiteLayout,
		H1,
		H2,
		H3,
		H4,
		H5,
		Header,
		Footer,
	} from '../../packages/src'
</script>

<Theme>
	<Header />

	<SiteLayout>
		<H1>Hello World</H1>

		<p>
			Lorem ipsum dolor sit amet, <a href="/">consectetur</a> adipiscing elit,
			sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut
			enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut
			aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit
			in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
			Excepteur sint occaecat cupidatat non proident, sunt in culpa qui
			officia deserunt mollit anim id est laborum.
		</p>

		<H2>Heading Two</H2>
		<H3>Heading Three</H3>
		<H4>Heading Four</H4>
		<H5>Heading Five</H5>

		<hr />
		<div>
			<p>
			Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
			eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad
			minim veniam, quis nostrud exercitation ullamco laboris nisi ut
			aliquip ex ea commodo consequat. Duis aute irure dolor in
			reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla
			pariatur. Excepteur sint occaecat cupidatat non proident, sunt in
			culpa qui officia deserunt mollit anim id est laborum.
			</p>
			<ul>
				<li>Hi</li>
				<li>Hello</li>
				<li>It's me</li>
			</ul>
		</div>

		<Card>
			<h3 slot="title">Card Heading</h3>

			<p>
			Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
			eiusmod tempor incididunt ut
			</p>
			<Button>Accept</Button>
		</Card>

		<div>
			<aside>
			<p>
				Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
				eiusmod tempor incididunt ut
			</p>
			</aside>
			<p>
			Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
			eiusmod tempor incididunt ut Lorem ipsum dolor sit amet, consectetur
			adipiscing elit, sed do eiusmod tempor incididunt ut Lorem ipsum dolor
			sit amet, consectetur adipiscing elit, sed do eiusmod tempor
			incididunt ut
			</p>
		</div>

		<div>
			<aside>
			<p>
				Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
				eiusmod tempor incididunt ut
			</p>
			</aside>
			<p>
			Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
			eiusmod tempor incididunt ut Lorem ipsum dolor sit amet, consectetur
			adipiscing elit, sed do eiusmod tempor incididunt ut Lorem ipsum dolor
			sit amet, consectetur adipiscing elit, sed do eiusmod tempor
			incididunt ut
			</p>
		</div>

		<hr />

		<form>
			<div>
				<div>
					<label for="text">Text</label>
					<Input />
				</div>
				<div>
					<label for="number">Number</label>
					<Input />
				</div>

				<div>
					<label for="email">Email</label>
					<Input />
				</div>
			</div>
			<div>
				<label for="textarea">Textarea</label>
				<TextArea id="textarea">Default value</TextArea>
			</div>
			<div>
				<label for="select">Select</label>
				<Select>
					<option value="one">One</option>
					<option value="two">One</option>
				</Select>
			</div>

			<Button>Submit</Button>
			<Button warn>Cancel</Button>
			<Button disabled>Disabled</Button>
			<Button>Button with long text</Button>
			<Button>Button &xrarr;</Button>
			<br />
			<Button small>Submit</Button>
		</form>
	</SiteLayout>

	<Footer />
</Theme>

<style>
	 @font-face {
        font-family: 'Dillan';
        src: url('/Dillan.woff') format('woff');
    }
</style>