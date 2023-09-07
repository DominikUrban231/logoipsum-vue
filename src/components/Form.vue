<template>
    <section v-if="isVisible" class="form">
        <form>
            <div>
                <label>IMIĘ<span>*</span></label>
                <input v-model="name" placeholder=" - wpisz -" type="text" name="name">
            </div>
            <div>
                <label>NAZWISKO<span>*</span></label>
                <input v-model="surname" placeholder=" - wpisz -" type="text" name="name">
            </div>
            <div>
                <label>E-MAIL<span>*</span></label>
                <input v-model="email" placeholder=" - wpisz -" type="text" name="name">
            </div>
            <p><span>*</span> - pola wymagane</p>
            <label class="checkbox-wrapper">
                <input class="checkbox" v-model="accept" type="checkbox" required>
                <p class="checkbox-text">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
            </label>
            <button @click.prevent="formSubmit({name, surname, email, accept})" type="submit">Wyślij</button>
            <p class="error" v-if="showErrorMessage">Proszę uzupełnić wymagane pola</p>

            <img @click="hideForm" src="./../assets/svg/close.svg" alt="">
        </form>
    </section>
</template>

<script>
export default {
    methods: {
        formSubmit(formObject) {
            if (this.name && this.email && this.email && this.accept) {
                console.log(formObject);
            } else {
                this.showErrorMessage = true;
            }
        },
        hideForm() {
            this.$emit('hide-form');        }
        
    },
    data() {
        return {
            name: '',
            surname: '',
            email: '',
            accept: false,
            showErrorMessage: false,
        }
    },
    props: {
        isVisible: false,
    }
}
</script>

<style lang="scss">
.form {
    position: relative;
    z-index: 1000;
    background-color: white;
    box-shadow: 0px 0px 30px #FF4359;
    border-radius: 40px;
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 30vw;
    padding: 70px 50px;
    label {
        display: flex;
        align-items: center;

    }
    input {
        display: block;
        padding: 0%;
        width: 100%;
        height: 2.5em;
        margin: 10px 0px;
        border-radius: 7px;
        border-color: #AFAFAF;
    }
    .checkbox-wrapper {
        display: flex;
        align-items: flex-start;
        .checkbox {
        height: 1em;
        margin: 0;
        .checkbox-text {
            margin: 0px;
        }
    }

    }
    span {
        color: #FF4359;
    }
    button {
        text-align: center;
        background-color: #FF4359;
        padding: 10px 30px;
        border-radius: 7px;
        box-shadow: 5px 5px 10px #FF4359(255, 0, 0);
        width: 100%;
        color: #FFFFFF;
        border: none;
    }
    // p {
    //     color: #FF4359;
    // }
    img {
        position: absolute;
        right: 25px;
        top: 25px;
        cursor: pointer;
    }
    .error {
        color: #FF4359;
        text-align: center;
    }
}
.hidden {
    visibility: hidden;
}
</style>