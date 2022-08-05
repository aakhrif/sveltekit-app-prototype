<script context="module" lang="ts">
    export async function load({ fetch }: any ): Promise<{}> {
        const res = await fetch('https://jsonplaceholder.typicode.com/posts')
        const products = await res.json()

        if (res.ok) {
            return {
                props: {
                    products
                }
            }
        }

        return {
            status: res.status,
            error: new Error('could not fetch products')
        }
    }
</script>

<script lang="ts">
    export let products: [{title: string}]
</script>

<div class="product">
    <ul>
        {#each products as product}
            <li><a href="#">
                {product.title}
            </a></li>
        {/each}
    </ul>
</div>

<style>

</style>