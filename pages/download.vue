<template>
    <div class="main_container">
        <main class="main">
            <div class="download">
                <ul class="normol_tab">
                    <li
                        @click="tabNum = 0"
                        :class="[this.tabNum == 0 ? 'on' : '']"
                    >
                        PC wallpaper
                    </li>
                    <li
                        @click="tabNum = 1"
                        :class="[this.tabNum == 1 ? 'on' : '']"
                    >
                        Mobile wallpaper
                    </li>
                </ul>

                <div class="download_box">
                    <div class="download_item">
                        <div class="download_item_pic" data-text="wallpaper01">
                            <img
                                src="~/assets/images/download/W540x960_01 (1).jpg"
                                alt=""
                            />
                        </div>
                    </div>
                </div>
            </div>

            <ul class="normol_page" style="display: none">
                <li class="normol_page_btn">3</li>
                <li class="normol_page_btn">2</li>
                <li class="normol_page_btn on">1</li>
                <li class="normol_page_btn prev"></li>
                <li class="normol_page_btn next"></li>
            </ul>
        </main>
    </div>
</template>
<script>
export default {
    data() {
        return {
            tabNum: 0,
        };
    },

    mounted() {
        window.onresize = () => {
            return (() => {
                // this.$route
                if (this.$route.path == "/download") {
                    this.sizeHnadler();
                }
            })();
        };
    },
    methods: {
        sizeHnadler() {
            // var download = document.querySelector('.download');
            var download_box = document.querySelector(".download_box");
            var download_item = document.querySelectorAll(".download_item");
            // 左右多家15間距
            var download_pic_width =
                document.querySelector(".download_item_pic").clientWidth + 30;
            // var download_pic_height = document.querySelector('.download_item_pic').clientHeight + 20;
            // console.log(download_pic_height);
            // var download_tab = document.querySelector('.download_tab');
            if (window.screen.width > 767) {
                let newItem_w = parseInt(
                    download_box.clientWidth / download_pic_width
                );
                download_item[0].style.width = "calc(100% / 4 )";
                for (var i = 0; i < download_item.length; i++) {
                    download_item[i].style.width =
                        "calc(100% /" + newItem_w + ")";
                }
            } else {
                for (var i = 0; i < download_item.length; i++) {
                    download_item[i].style.width = "";
                }
            }
        },
    },
};
</script>

<style>
</style>
