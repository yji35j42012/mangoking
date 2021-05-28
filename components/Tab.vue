<template>
    <ul class="normol_tab">
        <li
            :class="['normol_tab_item', tabNum == index ? 'on' : '']"
            @click="tabHandler(index)"
            v-for="(item, index) in tabName"
            :key="index"
        >
            {{ item }}
        </li>
    </ul>
</template>

<script>
export default {
    data() {
        return {
            tabNum: 0,
        };
    },
    props: {
        tabName: {
            type: Array,
            default: undefined,
        },
    },
    methods: {
        tabHandler(num) {
            this.$emit("changeTab", num);
            this.tabNum = num;
        },
    },
};
</script>
