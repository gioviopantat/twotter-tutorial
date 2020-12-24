<template>
    <div class="twoot-item" @click="emit(twoot.id)">
        <div class="user-profile__twoot">
            <div class="twoot-item__user">
                {{ username }}
            </div>
            <div class="twoot-item__content">
                {{ twoot.content }}
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "TwootItem",
    props: {
        username: {
            type: String,
            required: true
        },
        twoot: {
            type: Object,
            required: true
        }
    },
    methods: {
      emit(id) {
        // console.log(id);
         this.$emit('favorite', id)
      }
    }

};
</script>

<style>
.twoot-item {
    padding: 10px;
    background-color: white;
    border-radius: 5px;
    border: 2px solid #74a0d7;
    box-sizing: border-box;
    cursor: pointer;
    transition: all 0.25s ease;
    max-width: 1000px;
    height: auto;
    margin-bottom: 20px;
    margin-left: 20px;
}

.twoot-item:hover {
    transform: scale(1.05, 1.05);
}

.twoot-item__user {
    font-weight: bold;
}
</style>