
<script>

export default {
    name: 'AppFooter',

    data() {
        return {
            links: [
                {
                    title: 'DC COMICS',
                    list: [
                        'Characters',
                        'Comics',
                        'Movies',
                        'TV',
                        'Games',
                        'Videos',
                        'News'
                    ]
                },
                {
                    title: 'SHOP',
                    list: [
                        'Shop DC',
                        'Shop DC Collectibles'
                    ]
                },
                {
                    title: 'DC',
                    list: [
                        'Terms Of Use',
                        'Privacy Policy (New)',
                        'Ad Choices',
                        'Advertising',
                        'Jobs',
                        'Subscription',
                        'Talent Workshops',
                        'CPSC Cerfiticates',
                        'Ratings',
                        'Shop Help',
                        'Contact Us'
                    ]
                },
                {
                    title: 'SITES',
                    list: [
                        'DC',
                        'MAD Magazine',
                        'DC Kids',
                        'DC Universe',
                        'DC Power Visa',
                    ]
                },
            ],

            imgList: ['footer-facebook.png', 'footer-twitter.png', 'footer-youtube.png', 'footer-pinterest.png', 'footer-periscope.png',]
        }
    }
}

</script>

<template>

    <footer>

        <div id="footer-top">

            
            <div class="container">

                <img src="/img/dc-logo-bg.png" alt="Footer logo">
    
                <div class="links">
    
                    <div class="link-list" v-for="linkList in links">
                        <h2>
                            {{ linkList.title }}
                        </h2>
    
                        <ul>
                            <li v-for="currentLink in linkList.list">
                                <a href="#">{{ currentLink}}</a>
                            </li>
                        </ul>
                    </div>
    
                </div>
            </div>
        </div>

        <div id="footer-bottom">

            <div class="container">

                <div class="button">
                    SIGN-UP NOW!
                </div>

                <div class="social">

                    <div class="title">

                        <h2>
                            FOLLOW US
                        </h2>
                    </div>

                    <div class="img-list" v-for="(currentImg, index) in imgList">
                        <img :src="'/img/' + currentImg" :alt="'immagine ' + (index + 1)">
                    </div>
                </div>

            </div>
        </div>
        

    </footer>

</template>

<style lang="scss">

@use '../styles/variables' as *;

footer {
    color: white;

    #footer-top {
        background-image: url('/img/footer-bg.jpg');
        background-size: cover;
        padding: 44px 0px;
        overflow: hidden;

        .container {
            position: relative;
        }

        img {
            position: absolute;
            right: 10px;
            top:50%;
            transform: translateY(-50%);
        }

        .links {
            display: flex;
            align-items: flex-start;
            gap: 30px;

            .link-list {

                h2 {
                    font-size: 16px;
                }
            }
            

            ul {
                list-style-type: none;

                li {
                    font-size: 12px;

                    a {
                        text-decoration: none;
                        color: #959595;

                        &:hover {
                            color: white;
                        }
                    }
                }
            }
        }
    }

    #footer-bottom {
        background-color: #303030;
        padding: 30PX 0PX;

        .container {

            display: flex;
            justify-content: space-between;
            align-items: center;

            .button {
                padding: 16px;
                border: 2px solid $primary-color;
            }

            .social {
                display: flex;
                gap: 20px;

                .title {
                    display: flex;
                    align-items: center;
                    justify-content: center;

                    h2 {
                        color: $primary-color;
                        font-size: 16px;
                        align-items: center;
                    }
                }

                .img-list {
                    display: flex;
                    justify-content: center;
                    align-items: center;
                }
            }
        }

    }
}



</style>