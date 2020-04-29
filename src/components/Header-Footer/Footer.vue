<template>
    <footer>
        <div class="container">
            <div>
                <img :src="logoIcon" alt="footer logo" />
                <div class="contact">
                    <div>Call Us</div>
                    <div>555-555-5555</div>
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
import Logo from '../../assets/images/logo.png';

export default {
    data() {
        return {
            logoIcon: Logo,
        };
    },
};
</script>
