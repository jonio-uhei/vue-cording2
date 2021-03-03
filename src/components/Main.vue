<template>
    <main>
        <section id="information">
            <div class="information">
                <h2 class="information__title">お知らせ</h2>
                <ul class="information__block"
                    v-for="information in informations"
                    :key="information.id"
                >
                    <li class="information__list">
                        <a class="information__link" href="#">
                            <div class="information-flexbox">
                                <time class="information__date" datetime="">{{information.date}}</time><!--/.information__date-->
                                <p class="information__message">{{information.message}}</p><!--/.information__message-->
                            </div><!--/.information-flexbox-->
                            <p class="information__content">{{information.content}}</p><!--/.information__content-->
                        </a><!--/.information__link-->
                    </li><!--/.information__list-->
                </ul><!--/.information__block-->
            </div><!--/.information-->
        </section><!--/#information-->
        <section id="construct">
            <div class="construct">
                <h2 class="construct__title">施工事例</h2>
                <div class="construct__flexbox">
                    <ul class="construct__block"
                        v-for="construct in constructs"
                        :key="construct.id"
                    >
                        <li class="construct__list">
                            <div>
                                <img class="construct__image" :src="construct.image">
                                <p class="construct__title">{{construct.title}}</p><!--/.construct__message-->
                                <p class="construct__location">{{construct.location}}</p><!--/.construct__content-->
                                <a href="#"><img class="construct__details" :src="construct.details"></a>
                            </div>
                        </li><!--/.construct__list-->
                    </ul><!--/.construct__block-->
                </div><!--/.construct__flexbox-->
                <p class="performances"><a href="#">施工実績一覧</a></p><!--/.performances-->
            </div><!--/.construct-->
        </section><!--/#construct-->
        <section id="company">
            <div class="company">
                <a href="#"
                    v-for="company in companys"
                    :key="company.id"
                >
                    <img 
                        class="company__image"
                        :src="company.company"
                    ><!--/.section__image-->
                </a>
            </div><!--/.company-->
        </section><!--/#company-->
    </main>
</template>

<script>
export default{
    data:function(){
        return{
            informations:[
                {
                    message:'お知らせ',
                    date:'2020.11.17',
                    content:'本社打合せ室が完成しました。'
                },
                {
                    message:'お知らせ',
                    date:'2020.11.10',
                    content:'【メディア掲載】 住宅雑誌 2020年11月号'
                },
                {
                    message:'お知らせ',
                    date:'2020.11.01',
                    content:'ホームページが完成しました。'
                },
            ],
            constructs:[
                {
                    image:require('@/assets/images/construct1.png'),
                    title:'M様邸新築工事',
                    location:'埼玉県',
                    details:require('@/assets/images/more.png')
                },
                {
                    image:require('@/assets/images/construct2.png'),
                    title:'スカイビル',
                    location:'東京都',
                    details:require('@/assets/images/more.png')
                }
            ],
            companys:[
                {
                    company:require('@/assets/images/company.png')
                },
                {
                    company:require('@/assets/images/recruit.png')
                },
                {
                    company:require('@/assets/images/contact.png')
                },
            ]
        }
    }
}
</script>