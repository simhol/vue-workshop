<template>
    <div>
        <h1>Component slots</h1>

        <h2>Info</h2>
        <p>You can use slots to "move" HTML content from the parent's template to a specific place in the child component's template.</p>

        <h2>Exercise</h2>
        <div class="card-deck">
            <FancyCard>
                Hi there, {{number}}!
            </FancyCard>
            <FancyCard></FancyCard>
            <FancyCard>
                <template #default>
                    Hi there, {{number}}!
                </template>
                <template #abc>
                    Cheers, {{number}}!
                </template>
            </FancyCard>
        </div>
    </div>
</template>

<script>
    import FancyCard from "./FancyCard"

    export default {
        components: {
            FancyCard,
        },
        data() {
            return {
                number: 1336,
            }
        },
    }
</script>
