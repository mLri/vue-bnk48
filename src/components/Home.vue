<template>
    <div class="contain">

        <div class="head">
            <div class="bg-logo">
                <div class="logo">
                    <img src="https://www.bnk48.com/static/img/logo-bnk48.png" alt="BNK48">
                </div>
                <div class="navbar-main">
                    <Navbar></Navbar>
                </div>
            </div>
            
            
        </div>
        <!-- <Navbar></Navbar> -->

        <div class="main">
            <div class="band">
                <div class="img-band">
                    <img src="https://bnk48-www-html.s3-ap-southeast-1.amazonaws.com/uploads/images/file-70571c71a8e25e07df8b03517b015814.jpg" alt="">
                </div>

                <div class="aside">
                    <div class="aside-a">
                        <div class="schedule-wrok">
                            <img src="https://bnk48-www-html.s3-ap-southeast-1.amazonaws.com/uploads/images/file-0b351357d59118fb0ac4dd50eb342199.jpg" alt="">
                        </div>
                        <div class="question">
                            <img src="https://bnk48-www-html.s3-ap-southeast-1.amazonaws.com/uploads/images/file-7012d2094c261d74867a4aad509f8a84.jpg" alt="">
                        </div>
                    </div>

                    <div class="aside-b">
                        <div class="first-alabum">
                            <img src="https://bnk48-www-html.s3-ap-southeast-1.amazonaws.com/uploads/images/file-796fecd979ee6ea0186248aaa8d9f2be.png" alt="">
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="grid-update">
                <div class="update">
                    <h3>BNK48 Update</h3>
                    <div class="list-update">
                        <div class="date">
                            <p class="p-date">20</p> 
                            <p class="p-month">MAR</p>
                        </div>
                        <div class="detail-update">
                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Laborum, perspiciatis!
                        </div>
                        <div class="btn">
                            <input type="button" value="OFFICIAL NEWS">
                        </div>
                    </div>
                    <div class="list-update">
                        <div class="date">
                            <p class="p-date">23</p>
                            <p class="p-month">JUNE</p>
                        </div>
                        <div class="detail-update">
                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Laborum, perspiciatis!
                        </div>
                        <div class="btn">
                            <input type="button" value="OFFICIAL NEWS">
                        </div>
                    </div>
                    <div class="list-update">
                        <div class="date">
                            <p class="p-date">27</p>
                            <p class="p-month">DEC</p>
                        </div>
                        <div class="detail-update">
                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Laborum, perspiciatis!
                        </div>
                        <div class="btn">
                            <input type="button" value="OFFICIAL NEWS">
                        </div>
                    </div>
                </div>

                <div class="template-slide">
                    <Slides :images="images"></Slides>
                </div>
            </div>
            
            <div class="embed-responsive embed-responsive-16by9">
                <iframe 
                    src="https://www.youtube.com/embed/4TKCbe8jyRI?control=0&amp;show_info=0" 
                    allowfullscreen="allowfullscreen" 
                    class="embed-responsive-item">
                </iframe>
            </div>
            
            

            <Navbar></Navbar>
        </div>
    </div>
</template>

<script>
import Navbar from '@/components/Navbar'
import Slides from '@/components/Slides'

export default {
    components: {
        Navbar,
        Slides
    },
    data () {
        return {
            images: [
                { 'src': 'https://bnk48-www-html.s3-ap-southeast-1.amazonaws.com/uploads/images/file-f9d6d8cfbbabde65003a280b1e1b927a.jpg'},
                { 'src': 'https://bnk48-www-html.s3-ap-southeast-1.amazonaws.com/uploads/images/file-28b229acd33d11f890af7fa4bd99110b.jpg'},
                { 'src': 'https://bnk48-www-html.s3-ap-southeast-1.amazonaws.com/uploads/images/file-1b6910b9d02e5fb862d95e120284f4a9.jpg'},
                { 'src': 'https://bnk48-www-html.s3-ap-southeast-1.amazonaws.com/uploads/images/file-cac4266de32092197fffac0dbd63448b.png'},
                { 'src': 'https://bnk48-www-html.s3-ap-southeast-1.amazonaws.com/uploads/images/file-28b229acd33d11f890af7fa4bd99110b.jpg'}
            ]
        }
    }
}
</script>

<style scoped>


    .head {
        width: 100%;
        min-height: 60px;
        background-color: #c58ec3;
    }

    .logo {
        display: block;
        text-align: center;
    }

    .contain {
        background-color: #FEE7FF;
    }

    .main {
        max-width: 730px;
        margin: 0 auto;
    }

    .template-slide {
        max-width: 100%;
        /* background-color: red; */
    }

    .img-band img {
        width: 100%;
        height: auto;
    }

    .img-band img:hover {
        border: 4px solid #c791c5;
        margin: -4px -4px -4px -4px;
    }

    .aside {
        background-color: #FEE7FF;
        padding-top: 10px;
        padding-bottom: 10px;
    }

    .aside-a {
        display: grid;
        grid-template-columns: 1fr 1fr;
        margin-bottom: 10px;
    }

    .aside-a .schedule-wrok img,
    .aside-a .question img {
        width: 100%;
        height: auto;
    }

    .aside-b img {
        width: 100%;
        height: auto;
    }
    
    .update {
        outline: 5px dashed #e6c1e1;
        box-shadow: 0 0 0 5px #c794c0;
        margin: 5px;
        background-color: #fff;
        margin-bottom: 20px;
    }

    .update h3 {
        background-color: #e6c1e1;
        display: inline-block;
        padding: 0 20px;
        height: 30px;
        line-height: 30px;
        color: white;
        font-size: 16px;
    }

    .update h3::after {
        content: " ";
        position: absolute;
        width: 20px;
        margin-left: 0;
        border-top: 15px solid #e6c1e1;
        border-bottom: 15px solid #e6c1e1;
        border-right: 15px solid transparent;
    }

    .list-update {
        display: -webkit-box;
        margin: 15px;
        text-align: center;
    }

    .date {
        padding: 0 15px;
    }

    .btn {
        width: 35%;
        text-align: center;
    }

    .detail-update {
        word-wrap: break-word;
        width: 60%;
        color: #884785;
        padding-top: 5px;
    }

    .list-update input {
        color: #884785;
        background-color: white;
        border: 1px solid #884785;
        padding: 5px;
        margin-top: 8px;
    }

    p.p-date {
        font-size: 35px;
    }

    p.p-month {
        font-size: 12px;
    }

/* test video  */
    .embed-responsive {
        display: block;
        position: relative;
        width: 100%;
        padding-top: 56.25%;
        margin: 20px 0 20px 0;
    }

    .embed-responsive .embed-responsive-item {
        position: absolute;
        width: 100%;
        height: 100%;
        top: 0;
        /* bottom: 0; */
        /* left: 0; */
        /* border: 0; */
    }
/* end test video */

/* video trik */
    /* .embed-responsive {
        position: relative;
        display: block;
        width: 100%;
        padding: 0;
        overflow: hidden;
    }

    .embed-responsive-16by9:before {
        padding-top: 56.25%;
    }

    .embed-responsive:before {
        display: block;
        content: "";
    }

    .embed-responsive .embed-responsive-item {
        position: absolute;
        top: 0;
        bottom: 0;
        left: 0;
        width: 100%;
        height: 100%;
        border: 0;
    } */
/* end video trik */
    

    
    @media(min-width: 700px) {
        
        .band {
            display: grid;
            grid-template-columns: 4fr 1fr;
        }

        .aside-a {
            display: block;
            margin-top: 10px;
        }

        .schedule-wrok {
            margin-bottom: 10px;
        }

        .img-band {
            margin: 20px 20px 20px 0px;
        }

    }

    @media(min-width: 900px){

        .main {
            max-width: 1024px;
        }

        .bg-logo {
            max-width: 1024px;
            margin: 0 auto;
        }

        .logo {
            float: left;
        }

        .logo img {
            border-left: 1px solid #fff;
            border-right: 1px solid #fff;
        }

        .grid-update {
            display: grid;
            grid-template-columns: 52% 48%;
        }

         .update {
            margin: 0px 20px 0px 0px;
        } 

        /*
        .template-slide {
            width: 48%;
            float: left;
        } */

        .slide img {
            width: 100%;
            height: auto;
        }  
    }
</style>