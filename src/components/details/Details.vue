<template>
    <div class="details">
        <div class="details-wrapper">
            <div class="details-title">
                Informationen
            </div>

            <div class="details-info">
                <p>
                    "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur</p>

                <div class="details-contact d-flex">
                    <ul class="details-contact-list">
                        <li><img src="../../assets/email.svg"/><span><a href="mailto:KaiChristian.schrum@ovb.de">KaiChristian.schrum@ovb.de</a></span></li>
                        <li><img src="../../assets/smartphone.svg"/><span><a href="tel:+4915124084699">151-240-84699</a></span></li>
                        <li><img src="../../assets/phone.svg"/><span><a href="tel:+494032525125">40-325-251-25</a></span></li>
                        <li><img src="../../assets/web.svg"/><span><a href="www.ovb.de">www.ovb.de</a></span></li>
                        <li><img src="../../assets/location.svg"/><span><a href="https://www.google.com/maps/dir//Am+Stadtrand+50,+22047+Hamburg">Am Stadtrand 50, 22047 Hamburg</a></span></li>
                    </ul>
                </div>
            </div>

            <div>

                <div class="d-flex justify-content-center">
                    <iframe width="400" height="240"
                            src="https://maps.google.com/maps?width=400&amp;height=440&amp;hl=en&amp;q=Hamburg%20am%20stadtrand%2050+(OVB%20Hamburg%20)&amp;ie=UTF8&amp;t=&amp;z=13&amp;iwloc=B&amp;output=embed"
                            frameborder="0" scrolling="no" marginheight="0" marginwidth="0"></iframe>
                    <div style="position: absolute;width: 80%;bottom: 10px;left: 0;right: 0;margin-left: auto;margin-right: auto;color: #000;text-align: center;">
                    </div>
                </div>
                <br/>
            </div>

            <div class="details-title">
                Impressum
            </div>

            <div class="details-info">
                <p> Vermittler</p>
            </div>
        </div>
    </div>
</template>

<script>
    export default {}
</script>

<style scoped>

    .details {
        display: flex;
        align-items: center;
        justify-content: center;
        position: relative;
        left: -5px;
        width: 100%;
    }

    .details * {
        font-family: 'Poppins', sans-serif;
        overflow: hidden;
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
        /*border-left: 1px gray solid;*/
    }

    .details-contact-list {
        list-style-type: none;
        padding: 10px;
    }

    .details-contact-list li {
        font-size: 1rem;
        padding: 20px;
    }

    .details-contact-list li span a {
        padding-left: 10px;
        color: #003366;
    }

    .details-contact-list li span {
        padding-left: 10px;
    }

    .details-contact-list li:hover a {
        color: #78cc6d;
        transition: color 0.5s;
        text-decoration: none;
    }

    .details-wrapper {
        padding-left: 5px;
        height: 90%;
        background-color: white;
        width: 500px;
        position: absolute;
        left: 0;
        right: 0;
        border-top-right-radius: 2%;
        border-bottom-right-radius: 2%;
    }
</style>