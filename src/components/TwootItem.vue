<template>
    <div class="twoot-item">
        <div class="user-profile__twoot">
            <div class="twoot-item__user">
                {{ username }}
            </div>
            <div class="">
               <!-- 沒有這個東西 render 不出來 -->
                <!-- {{ twoot.content }} -->
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
        }
    },
    twoot: {
        // 沒有 content 上面拿不到
        type: Object,
        required: true
    }
};
</script>

<style>
.twoot-item {
    padding: 20px;
    background-color: white;
    border-radius: 5px;
    border: 1px solid #df3e8d;
    cursor: pointer;
    transition: all 0.25s ease;
}

.twoot-item:hover {
    transform: scale(1.1, 1.1);
}

.twoot-item__user {
    font-weight: bold;
}
</style>