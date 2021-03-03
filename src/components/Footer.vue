<template>
    <footer>
        <div class="footer__flexbox">
            <div class="list__flexbox order1">
                <ul
                    v-for="list in lists"
                    :key="list.id"
                >
                    <li><a href="#">{{list.link}}</a></li>
                </ul>
            </div><!--/.list__flexbox-->
            <a href="#"><img class="footer-logo order2" src="@/assets/images/footer-logo.jpg" alt=""></a>
        </div><!--/.footer__flexbox-->
        <p>Copyright ©︎ 2020 Aono Corporation.</p>
    </footer>
</template>

<script>
    export default{
        data:function(){
            return{
                lists:[
                    {
                        link:'企業理念'
                    },
                    {
                        link:'施工事例'
                    },
                    {
                        link:'採用情報'
                    },
                    {
                        link:'お問い合わせ'
                    },
                ]
            }
        }
        
    }
</script>