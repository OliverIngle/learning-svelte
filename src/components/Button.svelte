<script lang="ts">

    let numbers: number[] = [1, 2]

    function addNum() {
        numbers = [...numbers, numbers.length + 1]
    }

    $: sum = numbers.reduce((acc, curr) => {
        return acc + curr
    })

</script>

<button on:click={addNum}>{numbers.join(' + ')}</button>
<h1>{sum}</h1>