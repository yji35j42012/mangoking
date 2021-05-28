<template>
    <div class="main_container --portfolio">
        <div :class="['portfolio', this.nowTabName]">
            <Tab :tabName="tabsName" @changeTab="changeTabHandler"></Tab>

            <div class="portfolio_character">
                <div class="portfolio_character__item --mango --active">
                    <h1 class="name">
                        <img
                            src="~/assets/images/portfolio/character/mango_name.svg"
                            alt="萌果君"
                        />
                    </h1>
                    <div class="img_box">
                        <img
                            src="~/assets/images/portfolio/character/mango_img1.png"
                            alt="mangoking"
                        />
                        <img
                            src="~/assets/images/portfolio/character/mango_img2.png"
                            alt="料理"
                        />
                        <img
                            src="~/assets/images/portfolio/character/mango_img3.png"
                            alt="種植"
                        />
                        <img
                            src="~/assets/images/portfolio/character/mango_img4.png"
                            alt="探索"
                        />
                    </div>
                </div>
                <div class="portfolio_character__item --chabao">
                    <h1 class="name">
                        <img
                            src="~/assets/images/portfolio/character/chabao_name.svg"
                            alt="柴寶"
                        />
                    </h1>
                    <div class="img_box">
                        <img
                            src="~/assets/images/portfolio/character/chabao_img1.png"
                            alt="Chabao"
                        />
                        <img
                            src="~/assets/images/portfolio/character/chabao_img2.png"
                            alt="各種睡"
                        />
                        <img
                            src="~/assets/images/portfolio/character/chabao_img3.png"
                            alt="飛翔"
                        />
                        <img
                            src="~/assets/images/portfolio/character/chabao_img4.png"
                            alt="外送"
                        />
                    </div>
                </div>
                <div class="portfolio_character__item --hanji">
                    <h1 class="name">
                        <img
                            src="~/assets/images/portfolio/character/hanji_name.svg"
                            alt="夯吉"
                        />
                    </h1>
                    <div class="img_box">
                        <img
                            src="~/assets/images/portfolio/character/hanji_img1.png"
                            alt="Hanji"
                        />
                        <img
                            src="~/assets/images/portfolio/character/hanji_img2.png"
                            alt="挑食家"
                        />
                        <img
                            src="~/assets/images/portfolio/character/hanji_img3.png"
                            alt="釣魚"
                        />
                        <img
                            src="~/assets/images/portfolio/character/hanji_img4.png"
                            alt="逛街"
                        />
                    </div>
                </div>
                <ul class="normal_page" style="display: none">
                    <li class="normal_page_btn">3</li>
                    <li class="normal_page_btn">2</li>
                    <li class="normal_page_btn on">1</li>
                    <li class="normal_page_btn prev"></li>
                    <li class="normal_page_btn next"></li>
                </ul>
            </div>
            <div class="portfolio_gif r4c2">
                <ul class="r4c2_group">
                    <li
                        class="r4c2_item"
                        v-for="item in gifList"
                        :key="item.id"
                    >
                        <!-- <img :src="item.gifSrc" :alt="item.gifAlt" /> -->
                        <!-- <img :src="require(`~/assets/images/portfolio/gif/${item.gifSrc`)" /> -->
                        <img
                            :src="
                                require(`~/assets/images/portfolio/gif/${item.gifSrc}`)
                            "
                        />
                    </li>
                </ul>
            </div>
            <div class="portfolio_comics r4c2'">
                <ul class="r4c2_group">
                    <li class="r4c2_item">
                        <img
                            src="~/assets/images/portfolio/gif/G1.gif"
                            alt=""
                        />
                    </li>
                    <li class="r4c2_item">
                        <img
                            src="~/assets/images/portfolio/gif/G1.gif"
                            alt=""
                        />
                    </li>
                    <li class="r4c2_item">
                        <img
                            src="~/assets/images/portfolio/gif/G1.gif"
                            alt=""
                        />
                    </li>
                    <li class="r4c2_item">
                        <img
                            src="~/assets/images/portfolio/gif/G1.gif"
                            alt=""
                        />
                    </li>
                    <li class="r4c2_item">
                        <img
                            src="~/assets/images/portfolio/gif/G1.gif"
                            alt=""
                        />
                    </li>
                </ul>
            </div>
            <div class="portfolio_video r4c2">
                <div class="portfolio_video_box">
                    <div class="portfolio_video_item">
                        <iframe
                            width="100%"
                            height="100%"
                            src="https://www.youtube.com/embed/AddiTcSxc0E?controls=0"
                            title="YouTube video player"
                            frameborder="0"
                            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                            allowfullscreen
                        ></iframe>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>


<script>
export default {
    data() {
        return {
            tabsName: ["Character", "GIF", "Comics", "Video"],
            nowTabName: "Character",
            gifList: [
                {
                    id: 1,
                    gifSrc: "G1.gif",
                    gifAlt: "萌果君 gif",
                },
                {
                    id: 2,
                    gifSrc: "G2.gif",
                    gifAlt: "萌果君 gif",
                },
                {
                    id: 3,
                    gifSrc: "G3.gif",
                    gifAlt: "萌果君 gif",
                },
                {
                    id: 4,
                    gifSrc: "G4.gif",
                    gifAlt: "萌果君 gif",
                },
                {
                    id: 5,
                    gifSrc: "G5.gif",
                    gifAlt: "萌果君 gif",
                },
                {
                    id: 6,
                    gifSrc: "G6.gif",
                    gifAlt: "萌果君 gif",
                },
                {
                    id: 7,
                    gifSrc: "G7.gif",
                    gifAlt: "萌果君 gif",
                },
                {
                    id: 8,
                    gifSrc: "G8.gif",
                    gifAlt: "萌果君 gif",
                },
                {
                    id: 9,
                    gifSrc: "G9.gif",
                    gifAlt: "萌果君 gif",
                },
                {
                    id: 10,
                    gifSrc: "G10.gif",
                    gifAlt: "萌果君 gif",
                },
                {
                    id: 11,
                    gifSrc: "G11.gif",
                    gifAlt: "萌果君 gif",
                },
            ],
        };
    },
    computed() {
        
    },
    methods: {
        changeTabHandler(num) {
            this.nowTabName = this.tabsName[num];
        },
    },
};
</script>

<style>
</style>
