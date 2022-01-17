<script lang="ts">
    export let name: string;
    export let bio: string;
</script>

<div class="card">
    <div class="background"></div>
    <h1>{name}</h1>
    <p>{bio}</p>
</div>

<style>

    .card {
        height: 25rem;
        width: 20rem;
        border-radius: 20px;
        margin-right: 1rem;
        margin-bottom: 1rem;
        
        display: flex;
        flex-direction: column;
        align-content: flex-start;

        box-shadow: 0 3px 10px darkgrey;
        background: lightgrey;
    }

    .card > * {
        margin-left: 1rem;
        margin-right: 1rem;
        margin-top: 1rem;
    }

    h1 {
        font-weight: bold;
        font-size: 2rem;
    }

    .background {
        margin: 0;
        border-radius: 20px;
        flex-grow: 3;
        
        background: rgb(104,213,91);
        background: linear-gradient(42deg, rgba(104,213,91,1) 0%, rgba(0,212,255,1) 100%); 
    }

</style>