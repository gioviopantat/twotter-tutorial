<template>
    <div class="user-profile">
        <div class="user-profile__user-panel">
            <h1 class="user-profile__username">@{{ user.username }}</h1>
            <div class="user-profile__admin-badge" v-if="user.isAdmin">
                Admin
            </div>
            <div class="user-profile__follower-count">
                <strong>Followers: </strong> {{ followers }}
            </div>
        </div>
        <div class="user-profile__twoots-wrapper">
            <TwootItem v-for="twoot in user.twoots" :key="twoot.id" :username="user.username" :twoot="twoot" @favorite="toggleFavorite"/>
        </div>
    </div>
</template>

<script>
import TwootItem from "./TwootItem";

export default {
  name: 'UserProfile',
  components: { TwootItem },
  data() {
    return {
      followers: 0,
      user: {
        id: 1,
        username: '_hank4idiot',
        firstName: 'Hank',
        lastName: 'Lin',
        email: 'hanklin@gmail.com',
        isAdmin: true,
        twoots: [
            { id: 1, content: "Twotter is amazing" },
            { id: 2, content: "Don't forget to keep learning!" }
        ]
      }
    }
  },
  watch: {
    followers(newFollowerCount, oldFolloweCount) {
      if(oldFolloweCount < newFollowerCount) {
        console.log(`${this.user.username} has gained a follower`)
      }
      if(oldFolloweCount > newFollowerCount){
        console.log(`${this.user.username} has lost a follower`)
      }
    }
  },
  computed: {
    fullName() {
      return `${this.user.firstName} ${this.user.lastName}`;
    }
  },
  methods: {
    followUser() {
      this.followers++
    },
    unfollowUser() {
      this.followers--
    },
    toggleFavorite(id) {
      console.log(`Favorited Tweet #${id}`)
    }
  },
  mounted() {
    this.followUser()
    this.unfollowUser()
  }
}
</script>

<style>
.user-profile {
  display: grid;
  grid-template-columns: 1fr 3fr;
  max-width:100%;
  padding: 1em ;
}

.user-profile__twoots_wrapper {
    padding: 115px;
}

.user-profile__user-panel {
  display: flex;
  flex-direction: column;
  margin-left: 50px;
  padding: 20px;
  background-color: white;
  border-radius: 5px;
  border: 2px solid #74a0d7;
  line-height: 1cm;
  transition: all 0.25s ease;
}

.user-profile__user-panel:hover {
  transform: scale(1.1, 1.1);
}

.user-profile__admin-badge {
    background: rgb(112, 39, 185);
    color: white;
    border-radius: 5px;
    margin-right: auto;
    padding: 0 10px;
    font-weight: bold;
}

h1{
  margin: 5px;
}
</style>
