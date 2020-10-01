<template>
    <div>
        <small><code>Inserire "SI" per andare a capo / lasciare vuoto altrimenti</code></small>
        <input
                class="w-full form-control form-input form-input-bordered"
                type="text"
                :id="subField.name"
                :name="subField.name"
                :value="value"
                :placeholder="subField.placeholder"
                @input="$emit('input', $event.target.value)"

        >

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