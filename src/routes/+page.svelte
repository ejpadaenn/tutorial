<script>
    import Button from '$lib/Button.svelte'

    import { onMount } from 'svelte'

    onMount(() => {
        console.log('attaching first script')
        const script = document.createElement('script');
        script.src = 'https://cdn.jsdelivr.net/npm/particles.js@2.0.0/particles.min.js'
        document.body.appendChild(script);
    })

    onMount(() => {
        console.log('attaching second script')
        const script2 = document.createElement('script');
        script2.src = 'app.js'
        document.body.appendChild(script2);
    })

</script>

<html lang="en">
    <h1>WELCOME</h1>

    <Button/>

    <div id="particles-js"></div>
</html>

<style>
    #particles-js {
        height: 100%;
        width: 100%;
        z-index: -1;

        background-color: black;
    }
</style>