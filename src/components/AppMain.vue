<template>
    <main>
        <section>
            <h1> --&gt; Content goes here &lt;-- </h1>
        </section>
    </main>
</template>
<script>
export default {
    name: 'AppMain',
}
</script>
<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;

main {
    color: $primary_color;
    background-color: $black_color;
    font-family: $font;
}

section {
    @include contain;
    @include distance_section;
}
</style>