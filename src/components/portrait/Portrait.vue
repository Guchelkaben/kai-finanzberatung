<template>
    <div class="portrait-bg">
        <div>
            <div class="portrait-container">
                <img class="img-fluid portrait-header" src="../../assets/header-bg.png"/>
                <div class="portrait-info">
                    <div>
                        <img class="portrait-image" src="../../assets/profile.png"/>
                    </div>

                    <div>
                        <h2>
                            Kai-Christian Schrum
                        </h2>
                        <p class="portrait-subtitle">Finanzberater</p>
                        <p class="portrait-slogan">Anlegen, versichern, finanzieren - Ihr unabhängiger Finanzoptimierer</p>
                    </div>
                </div>
            </div>

            <div class="portrait-height"></div>
            <div class="d-flex flex-row justify-content-center">
                <a class="portrait-button col-6 d-flex align-items-center justify-content-center" position="left"
                   href="https://www.ovb.de/">
                    <span>
                        <span class="portrait-button-text left">Zur OVB</span>
                        <span class="portrait-button-icon"><i class="material-icons">
                        book
                    </i></span>
                    </span>

                </a>

                <a class="portrait-button col-6 d-flex align-items-center justify-content-center" href="tel:+4915124084699">
                    <span>
                        <span class="portrait-button-text ">Kontakt</span>
                    <span class="portrait-button-icon"><i class="material-icons">
                        phone
                    </i></span>
                    </span>
                </a>
            </div>
        </div>
    </div>
</template>

<script>
    export default {}
</script>

<style scoped>
    @media screen and (min-width: 680px ) {
        .portrait-bg {
            border-radius: 2%;
        }

        .portrait-header {
            border-radius: 2%;
        }
    }

    .portrait-bg {
        max-width: 500px;
        max-height: 615px;
    }

    .portrait-height {
        margin-bottom: 20px;
    }
    .portrait-bg {
        background-color: white;
        z-index: 1;
    }

    .portrait-container {
        position: relative;
        min-width: 320px;
    }

    .portrait-height {
        position: relative;
        visibility: hidden;
        width: 100%;
        top: 0;
        left: 0;
        max-height: 250px;
        min-height: 250px;
    }

    .portrait-button-text {
        margin-right: 10px;
        text-transform: uppercase;
        font-family: 'Poppins', sans-serif;
        font-size: .9rem;
    }

    .portrait-button-icon {
        position: absolute;
    }

    .portrait-slogan {
        font-size: .9rem;
        margin: 0 5px;
    }

    .portrait-slogan:before {
        content: "\"";
    }

    .portrait-slogan:after {
        content: "\"";
    }

    .portrait-info {
        position: absolute;
        text-align: center;
        top: 60%;
        right: 0;
        left: 0;
        margin: auto;
    }

    .portrait-image {
        border-radius: 50%;
        border: 3px white solid;
    }

    .portrait-subtitle {
        font-family: 'Poppins', sans-serif;
        margin-top: 10px;
        color: #78cc6d;
    }

    .portrait-button {
        color: #003366;
        position: relative;
        display: block;
        text-align: center;
        height: 70px;
        text-decoration: none;
        border-top: 1px rgba(197, 202, 213, .7) solid;
    }

    .portrait-button[position="left"]:after {
        content: '';
        position: absolute;
        right: 0;
        top: 0;
        width: 1px;
        height: 100%;
        background: -moz-radial-gradient(top, ellipse cover, rgba(197, 202, 213, .7) 0, rgba(255, 255, 255, 0) 70%);
        background: -webkit-radial-gradient(top, ellipse cover, rgba(197, 202, 213, .7) 0, rgba(255, 255, 255, 0) 70%);
        background: radial-gradient(ellipse at top, rgba(197, 202, 213, .7) 0, rgba(255, 255, 255, 0) 70%);
    }

    .portrait-button:hover {
        color: #78cc6d;
        transition: color 0.5s;
    }
</style>