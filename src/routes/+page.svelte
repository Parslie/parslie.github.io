<script>
    import Article from "../components/Article.svelte";
	import ExperienceList from "../components/ExperienceList.svelte";

    const work = [
        ["June 2023 - July 2023", "Cashier", "Kullbergs Jordgubbshandel"],
    ];
    const education = [
        ["August 2019 - Now", "Master of Science in Computer Science and Software Engineering", "Linköping University"],
        ["August 2016 - June 2019", "Game Development", "Ljud- & Bildskolan (Audio and Visual School)"],
    ];
</script>

<Article title="About me">
    <p>
        My name is Viktor Holta and I'm a software engineering student at Linköping University in Sweden.
        <!-- TODO: add more details -->
    </p>
</Article>

<Article title="Work experience">
    <ExperienceList items={work} />
</Article>

<Article title="Education">
    <ExperienceList items={education} />
</Article>