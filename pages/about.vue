<template>
    <div class="main_container">
        <!-- _author -->
        <div :class="['about', this.nowTabName]">
            <Tab :tabName="tabsName" @changeTab="changeTabHandler"></Tab>
            <div class="about_info">
                關於我們關於我們關於我們關於我們關於我們關於我們關於我們關於我們關於我們關於我們關於我們關於我們關於我們們關於我們關於我們關於我們關於我們關於我們
            </div>

            <!-- about Exhibition start -->
            <div class="scroll_box about_exhibition">
                <div class="about_box">
                    <div class="about_item">
                        <img
                            src="~/assets/images/about/about_pic1.png"
                            alt=""
                        />
                    </div>
                    <div class="about_item">
                        <img
                            src="~/assets/images/about/about_pic2.jpg"
                            alt=""
                        />
                    </div>
                    <div class="about_item">
                        <img
                            src="~/assets/images/about/about_pic3.jpg"
                            alt=""
                        />
                    </div>
                </div>
            </div>
            <!-- about Exhibition end -->

            <!-- about Author start -->
            <div class="about_author">
                <div class="about_author_txt">
                    <p>
                        關於我們關於我們關於我們關於我們關於我們關於我們關於我們關於我們關於我們關於我們關於我們關於我們關於我們們關於我們關於我們關於我們關於我們關於我們
                    </p>
                    <p>
                        關於我們關於我們關於我們關於我們關於我們關於我們關於我們關於我們關於我們關於我們關於我們關於我們關於我們們關於我們關於我們關於我們關於我們關於我們
                    </p>
                </div>
                <div class="about_author_pic">
                    <img src="~/assets/images/about/about_Author.png" alt="" />
                </div>
            </div>
            <!-- about Author end -->

            <!-- about contact start -->
            <div class="about_contact">
                <div class="about_contact_twTitle">歡迎圖像授權合作</div>
                <div class="about_contact_enTitle">Ascent Art Cretative</div>
                <div class="about_contact_info">
                    <p>萌果君 IvorWang</p>
                    <p>0915-646-775</p>
                    <p>mangoking08@gmail.com</p>
                </div>
                <div class="about_contact_artist">Artist : IvorWang</div>
                <div class="about_contact_end">
                    <p class="en">Thank you!</p>
                    <p class="tw">謝謝觀賞</p>
                </div>
            </div>

            <!-- about contact end -->
        </div>

        <ul class="normal_page" style="display: none">
            <li class="normal_page_btn">3</li>
            <li class="normal_page_btn">2</li>
            <li class="normal_page_btn on">1</li>
            <li class="normal_page_btn prev"></li>
            <li class="normal_page_btn next"></li>
        </ul>
    </div>
</template>


<script>
export default {
    data() {
        return {
            tabsName: ["exhibition", "author", "contact"],
            nowTabName: "exhibition",
        };
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
