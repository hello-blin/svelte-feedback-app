<script>
    import FeedbackItem from "./FeedbackItem.svelte";
    export const feedback = [
        {
            id: 1,
            rating: 10,
            text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. consequuntur vel vitae commodi alias voluptatem est voluptatum ipsa quae.",
        },
        {
            id: 2,
            rating: 9,
            text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. consequuntur vel vitae commodi alias voluptatem est voluptatum ipsa quae.",
        },
        {
            id: 3,
            rating: 8,
            text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. consequuntur vel vitae commodi alias voluptatem est voluptatum ipsa quae.",
        },
    ];
</script>

{#each feedback as fb (fb.id)}
    <h3>
        <FeedbackItem item={fb} />
    </h3>
{/each}
