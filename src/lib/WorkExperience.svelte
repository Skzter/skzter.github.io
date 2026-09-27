<script lang="ts">
    interface Props {
        title: string;
        organization: string;
        period: string;
        bullets: string[];
    }

    let { title, organization, period, bullets }: Props = $props();
</script>

<article>
    <div class="flex items-baseline">
        <h2>{title}</h2>
        <p>{period}</p>
    </div>
    <p>@ {organization}</p>
    <ul class="list-inside list-disc">
        {#each bullets as bullet}
            <li>{bullet}</li>
        {/each}
    </ul>
</article>
