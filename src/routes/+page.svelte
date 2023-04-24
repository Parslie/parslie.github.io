<script lang="ts">
	import Article from "../components/Article.svelte";
	import GridList from "../components/GridList.svelte";
	import LabeledList, { type LabeledListItem } from "../components/LabeledList.svelte";

	// TODO: fill out with more languages
	let languages = ["C#", "CSS", "HTML", "Javascript", "Python", "Typescript"];

	let work: LabeledListItem[] = [
    ["2022-present", "Software Maintainer @ WebbU"],
		["2021-2022", "Backend Developer @ WebbU"],
	];

	let school: LabeledListItem[] = [
    ["2019-present", "Linköpings Universitet (Linköping Univeristy)"],
		["2016-2019", "Ljud- och Bildskolan (Audio and Visual School)"],
	];
</script>

<Article>
	<h1>Welcome!</h1>
	<p>
		My name is Viktor Holta and I'm a software engineering student at Linköping 
		University in Sweden.
	</p>
	<!--p>
		If you need to contact me, you can reach me 
		at <a href="mailto:viktor.holta@outlook.com">viktor.holta@outlook.com</a>
	</p-->
</Article>

<Article>
	<h1>Programming Languages</h1>
	<p>
		These are the programming languages that I feel comfortable working with.
	</p>
	<GridList>
		{#each languages as lang}
			<span>{lang}</span>
		{/each}
	</GridList>
</Article>

<Article>
	<h1>Work</h1>
	<LabeledList items={work} />
</Article>

<Article>
	<h1>School</h1>
	<LabeledList items={school} />
</Article>