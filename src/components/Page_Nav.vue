<template>
    <div class="page-nav">

        <div class="left-contents">
            <div class="page-name">
                <p>{{PageName}}</p>
            </div>

            <div class="dropdown account-toggler">
                <button class="btn dropdown-toggle data-per-page" type="button" id="dropdownMenuButton1"
                    data-bs-toggle="dropdown" aria-expanded="false">
                    顯示10筆
                </button>
                <ul class="dropdown-menu" aria-labelledby="dropdownMenuButton1">
                    <li><a class="dropdown-item act-acc">顯示10筆</a></li>
                    <li><a class="dropdown-item ban-acc">顯示20筆</a></li>
                    <li><a class="dropdown-item ban-acc">顯示30筆</a></li>
                </ul>
            </div>
        </div>

        <div class="right-contents">
            <button type="button" class="btn btn-dark up-btn" v-if="Checked">
                <i class="bi bi-plus-lg"></i>
                上架
            </button>
            <button type="button" class="btn btn-dark down-btn" v-if="Checked">
                <i class="bi bi-plus-lg"></i>
                下架
            </button>
            <button type="button" class="btn btn-dark del-btn" v-if="Checked">
                <i class="bi bi-plus-lg"></i>
                刪除
            </button>
            <div class="input-group mb-3 input-group-sm">
                <span class="input-group-text" id="inputGroup-sizing-default"><i
                        class="bi bi-search"></i></span>
                <input type="text" class="form-control searcher" aria-label="Sizing example input"
                    aria-describedby="inputGroup-sizing-default">
            </div>
            <button type="button" class="btn create-btn" data-bs-toggle="modal"
                data-bs-target="#art-create-modal" v-if="func">
                <i class="bi bi-plus-lg"></i>
                新增
            </button>    
        </div>
    
    </div>

</template>

<script>
export default {
    props:['PageName','WithFunc','Checked']
}
</script>

<style lang='scss' scoped>
    @import '../assets/scss/basics/_BACK-colors.scss';
    @import '../assets/scss/components/Page_Nav.scss';
</style>