<script lang="ts">
    interface Props {
        title: string;
        link: string;
        period: string;
        bullets: string[];
    }

    let { title, link, period, bullets }: Props = $props();
</script>

<article>
    <div class="flex items-baseline">
        <h2>{title}</h2>
        <p>{period}</p>
    </div>
    <a href={link} target="_blank">{link}</a>
    <ul class="list-disc list-inside">
        {#each bullets as bullet}
            <li>{bullet}</li>
        {/each}
    </ul>
</article>
