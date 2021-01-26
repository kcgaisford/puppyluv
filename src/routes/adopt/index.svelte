<script>
    import DogType from './_DogTypes.svelte'
    let dogType = null;
</script>

<style>

</style>

<svelte:head>
    <title>Adopt Me</title>
</svelte:head>

{#if dogType === null}
    <DogType on:click={() => dogType = true}/>
{:else if dogType === true}
<div class="flex justify-center mt-10">
    <div class="w-1/3">

        <div class="bg-white p-5 rounded-md shadow-lg">
            <div class="text-3xl text-center semi-bold -mt-2 mb-2">What is Your Name?</div>
            <input type="text" id="name" class="w-full border-gray-300 border-2 rounded-md shadow-md p-2 text-2xl" />
            <div class="text-3xl text-center semi-bold my-2">What is Your Email?</div>
            <input type="email" id="email" class="w-full border-gray-300 border-2 rounded-md shadow-md p-2 text-2xl" />
            <div class="text-3xl text-center semi-bold my-2">How Many dogs do you want?</div>
            <input type="number" id="number" class="w-full border-gray-300 border-2 rounded-md shadow-md p-2 text-2xl" />
            <button class="p-3 bg-red-600 hover:bg-red-800 rounded-md text-white mt-3 w-full" data-event-title="Cocker / Ausie Mix" on:click={() => dogType = false}>Submit</button>
        </div>

    </div>
</div>
{:else if dogType === false}
<div class="flex justify-center mt-10">
    <div class="w-1/3">

        <div class="bg-white p-5 rounded-md shadow-lg">
            <div class="text-3xl text-center semi-bold mt-2 mb-2">Thanks for Adopting!</div>
        </div>

    </div>
</div>
{/if}

