<template>
    <section id="about" class="about">
        <div class="left">
            <img src="./../assets/img/aboutImage.jpg" alt="">
        </div>
        <div class="right">
            <h1>O MNIE</h1>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum. Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur magni dolores eos qui ratione voluptatem sequi nesciunt. Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam.</p>
        </div>
    </section>
</template>

<script>
export default {
}
</script>

<style lang="scss">
.about {
    display: flex;
    width: 100%;
    margin-top: 8vh;
    .left {
        width: 70%;
        img {
            max-width: 100%;
        }
    }
    .right {
        width: 30%;
        padding-inline: 80px;
        h1 {
            border-bottom: 1px solid red;
        }
    }
}
@media screen and (max-width: 1000px) {
    .about {
        flex-direction: column-reverse;
        .left {
            width: 100%;
        }
        .right {
            width: 100%;
            padding-inline: 0;
            h1 {
                max-width: fit-content;
                margin: auto;
                padding: 15px;
            }
            p {
                padding: 50px;
            }
        }
    }
}</style>