<template>
    <div>
        <div class="mobile-Responsive">
            <h2>{{note.smName}}</h2>
            <p ><a style=" color:gray; " href="">{{note.smName}}</a> {{note.description}}</p>
            <img style=" max-width: 200px; max-height: 150px; " :src=" note.url" alt="">
            <p>{{note.more}}</p>
            <div class="bottom">
                <div style="display:flex;">
                    <svg class="feather feather-twitter sc-dnqmqq jxshSx" xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="#dda77d" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true" data-reactid="1206">
                        <path d="M23 3a10.9 10.9 0 0 1-3.14 1.53 4.48 4.48 0 0 0-7.86 3v1A10.66 10.66 0 0 1 3 4s-4 9 5 13a11.64 11.64 0 0 1-7 2c9 5 20 0 20-11.5a4.5 4.5 0 0 0-.08-.83A7.72 7.72 0 0 0 23 3z"></path>
                    </svg>
                    <svg class="feather feather-package sc-dnqmqq jxshSx" xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="#dda77d" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true">
                        <path d="M12.89 1.45l8 4A2 2 0 0 1 22 7.24v9.53a2 2 0 0 1-1.11 1.79l-8 4a2 2 0 0 1-1.79 0l-8-4a2 2 0 0 1-1.1-1.8V7.24a2 2 0 0 1 1.11-1.79l8-4a2 2 0 0 1 1.78 0z"></path>
                        <polyline points="2.32 6.16 12 11 21.68 6.16"></polyline>
                        <line x1="12" y1="22.76" x2="12" y2="11"></line>
                        <line x1="7" y1="3.5" x2="17" y2="8.5"></line>
                    </svg>
                    <svg class="feather feather-github sc-dnqmqq jxshSx" xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="#dda77d" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true">
                        <path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"></path>
                    </svg>
                </div>
                <div style="display:flex;">
                    <svg class="feather feather-gitlab sc-dnqmqq jxshSx" xmlns="http://www.w3.org/2000/svg" width="26" height="26" viewBox="0 0 24 24" fill="none" stroke="#dda77d" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true">
                        <path d="M22.65 14.39L12 22.13 1.35 14.39a.84.84 0 0 1-.3-.94l1.22-3.78 2.44-7.51A.42.42 0 0 1 4.82 2a.43.43 0 0 1 .58 0 .42.42 0 0 1 .11.18l2.44 7.49h8.1l2.44-7.51A.42.42 0 0 1 18.6 2a.43.43 0 0 1 .58 0 .42.42 0 0 1 .11.18l2.44 7.51L23 13.45a.84.84 0 0 1-.35.94z"></path>
                    </svg>
                    <svg class="feather feather-feather sc-dnqmqq jxshSx" xmlns="http://www.w3.org/2000/svg" width="26" height="26" viewBox="0 0 24 24" fill="none" stroke="#dda77d" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true">
                        <path d="M20.24 12.24a6 6 0 0 0-8.49-8.49L5 10.5V19h8.5z"></path>
                        <line x1="16" y1="8" x2="2" y2="22"></line>
                        <line x1="17" y1="15" x2="9" y2="15"></line>
                    </svg>
                </div>
            </div>
        </div>
        <div id="theCard" ref="theCard" @click.stop="toggleRowActive" :class="{'active': active}">
            <div style="height: 100%;"> 
                <div class="left">
                    <p>
                        <a href="">{{note.smName}}</a> {{note.more}} </p>
                </div>
                <div class="center" >
                    <h2 style="font-family: 'Quicksand', sans-serif;color:black; margin-top:0;">{{note.smName}}</h2>
                    <p>{{note.description}}</p>
                    <div style="    display: flex;
    align-items: center;
    justify-content: center;
    height: 50%;"><img class="imazhet" style="max-height: 200px; max-width: 200px;" :src="note.url" alt=""></div>
                </div>
                <div class="theIcons">
                    <div style="display:flex;">
                        <svg class="feather feather-twitter sc-dnqmqq jxshSx" xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="#dda77d" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true" data-reactid="1206">
                            <path d="M23 3a10.9 10.9 0 0 1-3.14 1.53 4.48 4.48 0 0 0-7.86 3v1A10.66 10.66 0 0 1 3 4s-4 9 5 13a11.64 11.64 0 0 1-7 2c9 5 20 0 20-11.5a4.5 4.5 0 0 0-.08-.83A7.72 7.72 0 0 0 23 3z"></path>
                        </svg>
                        <svg class="feather feather-package sc-dnqmqq jxshSx" xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="#dda77d" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true">
                            <path d="M12.89 1.45l8 4A2 2 0 0 1 22 7.24v9.53a2 2 0 0 1-1.11 1.79l-8 4a2 2 0 0 1-1.79 0l-8-4a2 2 0 0 1-1.1-1.8V7.24a2 2 0 0 1 1.11-1.79l8-4a2 2 0 0 1 1.78 0z"></path>
                            <polyline points="2.32 6.16 12 11 21.68 6.16"></polyline>
                            <line x1="12" y1="22.76" x2="12" y2="11"></line>
                            <line x1="7" y1="3.5" x2="17" y2="8.5"></line>
                        </svg>
                        <svg class="feather feather-github sc-dnqmqq jxshSx" xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="#dda77d" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true">
                            <path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"></path>
                        </svg>
                    </div>
                    <div style="display:flex;">
                        <svg class="feather feather-gitlab sc-dnqmqq jxshSx" xmlns="http://www.w3.org/2000/svg" width="26" height="26" viewBox="0 0 24 24" fill="none" stroke="#dda77d" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true">
                            <path d="M22.65 14.39L12 22.13 1.35 14.39a.84.84 0 0 1-.3-.94l1.22-3.78 2.44-7.51A.42.42 0 0 1 4.82 2a.43.43 0 0 1 .58 0 .42.42 0 0 1 .11.18l2.44 7.49h8.1l2.44-7.51A.42.42 0 0 1 18.6 2a.43.43 0 0 1 .58 0 .42.42 0 0 1 .11.18l2.44 7.51L23 13.45a.84.84 0 0 1-.35.94z"></path>
                        </svg>
                        <svg class="feather feather-feather sc-dnqmqq jxshSx" xmlns="http://www.w3.org/2000/svg" width="26" height="26" viewBox="0 0 24 24" fill="none" stroke="#dda77d" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true">
                            <path d="M20.24 12.24a6 6 0 0 0-8.49-8.49L5 10.5V19h8.5z"></path>
                            <line x1="16" y1="8" x2="2" y2="22"></line>
                            <line x1="17" y1="15" x2="9" y2="15"></line>
                        </svg>
                    </div>
                </div>
            </div>
                <button>
                    <svg class="feather feather-search sc-dnqmqq jxshSx" xmlns="http://www.w3.org/2000/svg" width="20" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true" data-reactid="1001">
                        <circle cx="11" cy="11" r="8"></circle>
                        <line x1="21" y1="21" x2="16.65" y2="16.65"></line>
                    </svg>
                </button>
            </div>
        </div>
</template>
<script>
export default {
    name: "card",
    props: ['note', 'active', 'index'],
    methods: {
        toggleRowActive() {
            this.$emit('newactive', this.index);
        },
    },
};
</script>
<style lang="scss" scoped>
#mobile {
    display: none;
}

/*#theCard{
  position: relative;
  background-color: white;
  padding:20px;
  border-radius:10px;
  margin:10px 10px 0 10px;
  cursor: pointer;
  
}

#theCard.active{
  .left{
    display: flex;
    animation: slide-left .5s cubic-bezier(.25, .46, .45, .94) both;
  }
  .theIcons{
    display: flex;
  }
  button{
    display: flex;
  }
}

.left{
  padding:0 20px;
  display: none;
}
.theIcons{
  display: none;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  svg{
    padding:10px;
  }
}
button{
  display: none;
  position: absolute;
  padding:10px;
  outline:none;
  bottom: -20px;
  left:calc(50% - 10px);
  border-radius:50px;
  border:none;
  background-color: #d6a37b;
  cursor: pointer;
  svg{
    stroke:white;
  }
}*/
.mobile-Responsive {
    display: none;
}

#theCard {
    position: relative;
    margin: 15px;
    box-shadow: 0 5px 20px 0px rgba(82, 82, 82, 0.5);
    background-color: white;
    cursor: pointer;
    opacity: 0.5;
    padding: 0 10px;
    border-radius: 10px;
    height: 380px;
}

#theCard.active {
    border-radius: 0;
    align-items: center;
    justify-content: center;
    padding-left: 0;
    padding-right: 0;
    margin: 15px 220px 30px 220px;
    opacity: 1;

    .left {
        animation: slide-left .5s cubic-bezier(.25, .46, .45, .94) both;
        opacity: 1;
    }

    .theIcons {
        animation: slide-right .5s cubic-bezier(.25, .46, .45, .94) both;
        opacity: 1;
    }

    button {
        display: flex;

        &:hover {
            animation: myfirst .2s linear forwards;
        }
    }
}

.left {
    position: absolute;
    height: 100%;
    display: flex;
    border-radius: 10px 0 0 10px;
    align-items: center;
    background: white;
    left: 0;
    opacity: 0;
    height: 100%;
    z-index: 0;
    justify-content: center;
    width: 200px;
    white-space: normal;

    p {
        text-align: center;
        margin: 10px 0 0 0;
        max-width: 200px;
        padding: 10px;
        overflow-y: scroll;
        max-height: 300px;

        a {
            color: #8e8989;

            &:hover {
                color: #565656;
            }
        }
    }

    ::-webkit-scrollbar {
        display: none;
    }
}

.center {
    background: white;
    align-items: center;
    height: 100%;
    z-index: 10;
    width: 300px;
}

h2 {
    font-weight: 500;
    margin: 0;
    padding-top: 20px;
}

.imazhet {
    -webkit-user-select: none;
}

.theIcons {
    background: white;
    position: absolute;
    height: 100%;
    top: 0;
    width: 200px;
    border-radius: 0px 10px 10px 0px;
    right: 0;
    opacity: 0;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;

    svg {
        padding: 5px;
    }
}

button {
    display: none;
    position: absolute;
    padding: 10px;
    outline: none;
    bottom: -20px;
    left: calc(50% - 10px);
    border-radius: 50px;
    border: none;
    background-color: #d6a37b;
    cursor: pointer;

    svg {
        stroke: white;
    }
}

@keyframes slide-left {
    0% {
        transform: translateX(0)
    }

    100% {
        transform: translateX(-199px)
    }
}

@keyframes slide-right {
    0% {
        transform: translateX(0)
    }

    100% {
        transform: translateX(199px)
    }
}

@keyframes myfirst {
    0% {
        top: calc(100% - 18px)
    }

    100% {
        top: calc(100% - 24px)
    }
}

@media only screen and (max-width: 769px) {
    .mobile-Responsive {
        background-color: white;
        align-items: center;
        display: inherit;
        max-width: max-content;
        padding: 20px;
        border-radius: 20px;
        margin: 10px 0;
    }

    .bottom {
        >div {
            display: flex;
            align-items: center;
            justify-content: center;
        }

        svg {
            padding: 10px;
        }
    }

    #theCard {
        -webkit-appearance: none;
        display: none;
    }
}
@media only screen and (min-width: 770px) and (max-width: 1573px){
  @keyframes slide-left {
    0% {
        transform: translateX(0)
    }

    100% {
        transform: translateX(-195px)
    }
}

@keyframes slide-right {
    0% {
        transform: translateX(0)
    }

    100% {
        transform: translateX(195px)
    }
}
}
</style>