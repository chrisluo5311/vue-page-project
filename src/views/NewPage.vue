<template>
    <div class="row">
        <div class="col-4">
            <div class="list-group">
            <router-link to="/newpage/a" href="#" class="list-group-item list-group-item-action">
                前往A頁面
            </router-link>
            <router-link to="/newpage/b" href="#" class="list-group-item list-group-item-action">
                前往B頁面
            </router-link>
            <router-link to="/newpage/namedView/c2a" href="#" class="list-group-item list-group-item-action">
                命名路由c2a
            </router-link>
            <router-link to="/newpage/namedView/a2b" href="#" class="list-group-item list-group-item-action">
                命名路由a2b
            </router-link>
            <router-link to="/newpage/dynamicRouter" href="#" class="list-group-item list-group-item-action">
                動態路由($route)
            </router-link>
            <router-link to="/newpage/dynamicRouterByProps" href="#" class="list-group-item list-group-item-action">
                動態路由(props)
            </router-link>
            <router-link to="/newpage/routerNavigation" href="#" class="list-group-item list-group-item-action">
                路由導覽
            </router-link>
            </div>
        </div>

        <div class="col-8">
            <router-view>
            </router-view>
        </div>
    </div>
</template>