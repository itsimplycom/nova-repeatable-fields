<template>
    <div>
        <input :id="subField.name"
               :name="subField.name"
               onwheel="this.blur()"
               type="number"
               step="0.01"
               min="0"
               class="w-full form-control form-input form-input-bordered"
               :value="value"
               :placeholder="subField.placeholder"
               @input="$emit('input', $event.target.value)"
        />

    </div>

</template>

<script>
    export default {

        props: [
            'subField',
            'value'
        ]
    }

</script>

<style scoped>
    input[type="number"]::-webkit-outer-spin-button,
    input[type="number"]::-webkit-inner-spin-button {
        -webkit-appearance: none;
        margin: 0;
    }

    input[type="number"] {
        -moz-appearance: textfield;
    }
</style>