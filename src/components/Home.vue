<template>
    <v-container fluid>
        <v-form>
            <v-file-input
                label="Selecione as legendas"
                prepend-icon="mdi-message-text"
                append-outer-icon="mdi-send"
                outlined
                multiple
                chips
                v-model="files"
                @click:append-outer="processSubtitles"
            />
        </v-form>
        <div class="pills">
            <pill v-for="word in groupedWords" :key="word.name" :name="word.name" :amount="word.amount" />
        </div>
    </v-container>
</template>

<script>
import Pill from './Pill.vue';
export default {
    name: "Home",
    components: {
        Pill,
    },
    data() {
        return {
            files: [],
            groupedWords: [
                {
                    name: "are",
                    amount: 800,
                },
                {
                    name: "the",
                    amount: 700,
                },
                {
                    name: "best",
                    amount: 600,
                },
                {
                    name: "in",
                    amount: 500,
                },
                {
                    name: "world",
                    amount: 300,
                },
                {
                    name: "and",
                    amount: 200,
                },
                {
                    name: "you",
                    amount: 100,
                },
            ],
        };
    },
    methods: {
        processSubtitles() {
            console.log(this.files);
        }
    },
};
</script>

<style lang="scss" scoped>
.pills {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
}
</style>