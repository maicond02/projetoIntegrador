<template>
    <div class="grid-class">
        <div class="item">
            <br><br><h3>LOGIN</h3>
            <div class="field col-12 md:col-4">
                <InputText id="user" placeholder="Usuário"/>
            </div>
            <div class="field col-12 md:col-4">
                <InputText id="senha" placeholder="Senha" type="password"/>
            </div>
            <button @click="login">Login</button>
            <transition-group name="p-messages" tag="div">
                <Message v-for="msg of messages" :severity="msg.severity" :key="msg.content">{{msg.content}}</Message>
            </transition-group>
        </div>
    </div>
</template>

<script>

    export default {
        data(){
            return{
              user: '',
              password:'',
              to:'/home',
              messages:[],
            }
        },
        methods:{
            login(){
                let user = document.getElementById('user').value
                let senha = document.getElementById('senha').value
                if(user === 'admin' && senha === '123'){
                    location.href = "home"
                }else{
                    return this.mensagem()
                }
            },
            mensagem(){
                this.messages = [
				{severity: 'error', content: 'Usuário ou Senha Incorretos'}
            ]
            },
        }
    }

</script>

<style scoped>
.grid-class{
    width: 100%;
    height: 100vh;
    border: 1px solid black;
    display: flex;
    justify-content: center;
    text-align: center;
    align-items: center;
    background-color: rgb(7, 0, 17);
}

a{
    text-decoration: none;
}

p{
    color: rgb(0, 0, 0);
}

.item{
    background-color: rgb(255, 255, 255);
    height: 40%;
    width: 80%;
    border-radius: 10px;
}

button{
    background-color: white;
    color: rgb(255, 255, 255);
    cursor: pointer;
    height: 40px;
    width: 80px;
    background-color: rgb(21, 0, 49);
    border: solid 1px rgb(21, 0, 49);
    border-radius: 10px;
}
</style>