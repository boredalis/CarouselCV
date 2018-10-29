<template>
    <div id="app">
        <img class="bg" style="-webkit-user-select: none;"src="https://images.unsplash.com/photo-1449247709967-d4461a6a6103?ixlib=rb-0.3.5&amp;ixid=eyJhcHBfaWQiOjEyMDd9&amp;s=1053a3cdbabdd85102b762b3a05966ae&amp;auto=format&amp;fit=crop&amp;w=1502&amp;q=80">
        <div class="container" ref="container">
            <div class="carousel-item-spacer">
                <p>This is a spacer</p>
            </div>
            <div style="display:flex;">
                <card v-for="(note,index) in notes" :class="noteClass(index)" :active="index === activeIndex" :index="index" :note="note" @newactive="hapuSusam(index)"></card>
            </div>
            <div class="carousel-item-spacer">
                <p>This is a spacer</p>
            </div>
        </div>
        <div class="footer">
            <img src="https://upload.wikimedia.org/wikipedia/en/d/dc/MichaelScott.png"style="
            position: relative;
            height: 60px;
            width: 50px;
            border-radius: 5px;
            ">
            <h2>Altin Selimi</h2>
            <h3>Developer</h3>
            <a href=""><svg class="feather feather-linkedin sc-dnqmqq jxshSx" xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="white" stroke="white" stroke-width="0" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true" data-reactid="696">
                <path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"></path>
                <rect x="2" y="9" width="4" height="12"></rect>
                <circle cx="4" cy="4" r="2"></circle>
            </svg></a>
        </div>
    </div>
</template>
<script>
// @ is an alias to /src
import card from '@/components/card.vue'

export default {
  name: 'home',
  components: {
      card
  },
  data() {
    return {
      activeIndex: 0,
      notes: [{
        smName: 'Mydevportfol.io',
        url: 'https://chippd.github.io/deskportfolio/devportfolio.png',
        description: 'A portfolio site builder for developers',
        more: 'uses ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. '},
        {smName: 'Jobb.ie',
        url: 'https://chippd.github.io/deskportfolio/jobbie.png',
        description: 'A jobs site aggregator/scraper',
        more: 'lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. '},
        {smName: 'Slack chat bot',
        url: 'https://chippd.github.io/deskportfolio/slack.png',
        description: 'For checking domain availability in Slack',
        more: 'lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. '}]
    }
  },
  methods: {
    noteClass(index) {
        return `card-${index+1}`;
    },
    hapuSusam(index) {
        this.activeIndex = index;
        let element = this.$refs.container;
        let target = document.querySelector(`.card-${index+1}`);
        setTimeout(() => {
          target.scrollIntoView({behavior: "smooth",block: "center",inline: "center"});
        }, 0);
    },
  }
}
</script>
<style lang="scss">
body {
    position: relative;
    margin: 0;
    max-width: 100vw;
    overflow: hidden;
    height: 100vh;
    box-sizing: content-box;
}

.bg {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 120%;
    z-index: 0;
}

.container {
    position: relative;
    overflow-x: scroll;
    display: flex;
    width: 100vw;
    //padding-top: 40px;
}

.container::-webkit-scrollbar {
    display: none;
}

.carousel-item-spacer {
    min-width: 400px;
    visibility: hidden;
    height: 300px;
}

.footer {
    padding: 40px 0;
    position: relative;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    margin-left: 40px;

    h2 {
        margin: 0;
        margin-top: 10px;
        font-size: 18px;
        color: black;
        font-weight: 500;
    }

    h3 {
        margin-top: 5px;
        margin-bottom: 10px;
        font-size: 15px;
        color: black;
        font-weight: 400;
    }

    svg {
        padding: 2px;
        border-radius: 3px;
        border: solid 1px gray;
        background-color: black;
    }
}

#app {
    font-family: "Avenir", Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    text-align: center;
    color: #2c3e50;
    height: 100vh;
    display: flex;
    flex-direction:column;
    justify-content:space-between;
    position: relative;
}
</style>