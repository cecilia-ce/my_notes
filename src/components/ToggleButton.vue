<template>
    <div>
      <input type="checkbox" class="toggleBtn" id="chk" />
      <label class="label" for="chk">
        <img id="lua" :src="luaSrc" />
        <img id="sol" :src="solSrc" />
        <div class="ball"></div>
      </label>
    </div>
</template>

<script>
    export default {
        name: 'ToggleButton',
        data(){
            return {
                luaSrc: '/img/lua.png',
                solSrc: '/img/sol.png'
            }
        }
    }
</script>

<style scoped>

   

    /* body {
    background-color: #fafafa;
    display: flex;
    align-items: center;
    justify-content: center;

    height: 100vh;
    margin: 0;
    transition: background 0.2s linear;
    } */

    /* body.dark {
    background: #292c35;
    } */

    .toggleBtn {
    opacity: 0;
    position: absolute;
    }

    .label {
    background-color: #FA00FF;
    border-radius: 50px;
    cursor: pointer;
    display: flex;
    justify-content: space-between;
    align-items: center;

    padding: 5px;
    position: relative;
    height: 16px;
    width: 33px;
    transform: scale(1.5);
    margin: 10px;

    }


    .label .ball {
    background-color: #823983;
    border-radius: 50%;
    position: absolute;
    top: 1px;
    left: 1px;
    right: 1px;
    bottom: 1px;
    height: 90%; 
    width: 45%;
    transform: translateX(0px);
    transition: transform 0.2s linear;
    }

    .toggleBtn:checked + .label .ball {
    transform: translateX(16px);
    }

    #lua {
        width: 50%;
    }

    #sol {
        width: 50%;
    }

</style>
