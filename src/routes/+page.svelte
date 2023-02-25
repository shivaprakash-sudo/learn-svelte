<script>
    import Nested from './Nested.svelte';
    import Info from './Info.svelte';

    const details = {
        name: "Shiva",
        link: "https://linkedin.com/in/shiva-pendem"
    };
</script>

<h3>Props</h3>
<Nested answer={42}/>

<h3>Default Props</h3>
<Nested />

<h3>Object props</h3>

<Info name={details.name} link={details.link}/>

<h3>Spread props</h3>

<Info {...details}/>