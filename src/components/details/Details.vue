<template>
    <div class="details">
        <div class="details-wrapper">
            <div class="details-title">
                Informationen
            </div>

            <div class="details-info">
                <div class="details-scroll">
                    <p>
                        "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur</p>
                    <div class="details-contact d-flex">
                        <ul class="details-contact-list">
                            <a href="mailto:KaiChristian.schrum@ovb.de">
                                <li><img src="../../assets/email.svg"/><span>KaiChristian.schrum@ovb.de</span></li>
                            </a>
                            <a href="tel:+4915124084699">
                                <li><img src="../../assets/smartphone.svg"/><span>+49 151 240 84 6 99</span></li>
                            </a>
                            <a href="tel:+494032525125">
                                <li><img src="../../assets/phone.svg"/><span>+49 40 325 251 25</span></li>
                            </a>
                            <a href="https://www.ovb.de">
                                <li><img src="../../assets/web.svg"/><span>www.ovb.de</span></li>
                            </a>
                            <a href="https://www.google.com/maps/dir//Am+Stadtrand+50,+22047+Hamburg">
                                <li><img src="../../assets/location.svg"/><span>Am Stadtrand 50, 22047 Hamburg</span>
                                </li>
                            </a>
                        </ul>
                    </div>

                    <div>
                        <div class="d-flex justify-content-center">
                            <iframe class="google-iframe"
                                    src="https://maps.google.com/maps?width=400&amp;height=440&amp;hl=en&amp;q=Hamburg%20am%20stadtrand%2050+(OVB%20Hamburg%20)&amp;ie=UTF8&amp;t=&amp;z=13&amp;iwloc=B&amp;output=embed"
                                    frameborder="0" scrolling="no" marginheight="0" marginwidth="0"></iframe>
                        </div>
                    </div>
                    <br/>
                </div>
            </div>
            <div :class="[!isEnd ?  'show-scroll' : 'show-not-scroll']">
                <img class="small-icon" src="../../assets/arrowdown.svg"/>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                isEnd: false,
                element: null,
            }
        },
        methods: {
            handleScroll() {
                console.log(this.element.scrollTop);
                this.isEnd = this.element.scrollTop === 335;
            }
        },
        mounted() {
            this.element = document.getElementsByClassName("details-scroll")[0];
            this.element.addEventListener('scroll', this.handleScroll);
        },
        destroyed() {
            this.element.removeEventListener('scroll', this.handleScroll);
        }
    }
</script>

<style scoped>
    .show-scroll {
        display: none !important;
    }

    .show-not-scroll {
        display: none !important;
    }

    @media screen and (min-width: 680px ) {
        .details-wrapper {
            border-radius: 0.8%;
        }
    }

    @media screen and (min-width: 1200px ) {
        .details {
            left: -5px;
            position: relative;
        }

        .details-wrapper {
            border-top-right-radius: 2%;
            border-bottom-right-radius: 2%;
            padding-left: 5px;
            position: absolute;
            margin: auto;
            max-height: 465px;
            top: 0;
            left: 0;
            bottom: 0;
            right: 0;
        }

        .details {
            left: -5px;
        }

        .details-info {
            position: relative;
            height: 85%;
        }

        .details-scroll {
            overflow-y: scroll;
            height: 100%;
            border-bottom: 2px gray solid;
        }

        ::-webkit-scrollbar {
            display: none;
        }

        .show-scroll {
            display: flex !important;
            justify-content: center;
            position: absolute;
            top: 93%;
            left: 0;
            bottom: 0;
            right: 0;
        }

        .small-icon {
            height: 20px;
        }
    }

    .details {
        display: flex;
        align-items: center;
        justify-content: center;
        position: relative;
        width: 100%;
        max-width: 500px;
        margin-top: 10px;
    }

    .details-wrapper {
        background-color: white;
        left: 0;
        right: 0;
    }

    .details-contact-list {
        list-style-type: none;
        padding: 3px;
    }

    .details * {
        font-family: 'Poppins', sans-serif;
    }

    .details-title {
        padding: 15px;
        border-bottom: 1px gray solid;
        font-size: 1.5rem;
    }

    .details-info:before {
        content: '';
        position: absolute;
        left: 0;
        top: 0;
        width: 1px;
        height: 110%;
        background: -moz-radial-gradient(top, ellipse cover, rgba(197, 202, 213, .7) 0, rgba(255, 255, 255, 0) 70%);
        background: -webkit-radial-gradient(top, ellipse cover, rgba(197, 202, 213, .7) 0, rgba(255, 255, 255, 0) 70%);
        background: radial-gradient(ellipse at top, rgba(197, 202, 213, .7) 0, rgba(255, 255, 255, 0) 70%);
    }

    .details-info {
        margin-left: 10px;
        position: relative;
        padding: 10px;
        font-size: 0.9rem;
    }

    .details-contact-list li {
        font-size: 1rem;
        padding: 15px;
    }

    .details-contact-list li span {
        padding-left: 10px;
    }

    .details-contact-list a {
        color: #003366;
        font-family: 'Poppins', sans-serif;
    }

    .details-contact-list a:hover {
        color: #78cc6d;
        transition: color 0.5s;
        text-decoration: none;
    }

    .google-iframe {
        width: 100%;
        height: 250px;
        bottom: 10px;
        color: #000;
        text-align: center;
    }
</style>