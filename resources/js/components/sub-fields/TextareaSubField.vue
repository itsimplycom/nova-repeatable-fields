<template>
    <div>
        <small><code>&lt;br&gt; Per andare a capo</code></small>
        <textarea
                class="w-full shadow-inner p-4 border-0"
                :id="subField.name"
                :name="subField.name"
                :value="value"
                :placeholder="subField.placeholder"
                @input="$emit('input', $event.target.value)"

        >

        </textarea>
    </div>

</template>

<script>

    export default {
        props: [
            'subField',
            'value'
        ],

    }
</script>
<style scoped>
    small {
        padding-left: 10px;
        margin-bottom: 5px;
    }

    textarea {
        color: #7c858e;
        height: 150px;
        border: 1px solid #bacad6;
        border-radius: .5rem;
    }
</style>