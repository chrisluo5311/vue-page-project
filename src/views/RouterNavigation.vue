<template>
    <button type="button" @click="getRoute">getRoute</button>
    <button type="button" @click="push">push</button>
    <button type="button" @click="replace">Replace</button>
    <button type="button" @click="go">Go</button>
    <hr />
    <button type="button" @click="addRoute">新增路由</button>
</template>

<script>
export default {
    methods: {
        //包含歷史紀錄
        push() {
            //seed:9ba9e64ad878cf8b
            // this.$router.push('/newpage/dynamicRouter/9ba9e64ad878cf8b')
            this.$router.push({
                name:'about',
            });
        },
        //沒有包含歷史紀錄
        replace(){
            this.$router.replace({
                name:'about',
            });
        },
        //操作歷史紀錄
        go(){
            //副值往前一頁
            this.$router.go(-1);
        },
        getRoute(){
            //路由方法：https://next.router.vuejs.org/zh/api/#router-方法
            //路由屬性：https://next.router.vuejs.org/zh/api/#routelocationnormalized
            console.log(this.$route);
            console.log(this.$router);
        },
        //臨時新增路由
        //值與路由表一樣
        addRoute(){
            this.$router.addRoute({
                path: '/newabout',
                name: 'newabout',
                // route level code-splitting
                // this generates a separate chunk (about.[hash].js) for this route
                // which is lazy-loaded when the route is visited.
                component: () => import(/* webpackChunkName: "about" */ './AboutView.vue')
            })
        }
    }
}
</script>