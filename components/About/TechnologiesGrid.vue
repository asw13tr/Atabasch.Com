<template>
        <ColoredTitle title="Kullanılan Teknolojiler" size="3" reverse/>
        <div class="row g-3">

            <div class="col-12 col-sm-6 col-md-4 col-lg-3" v-for="(i, k) in items" :key="k">
                <div class="technologyItem p-2 box-dark-blue h-100">
                    <div class="d-flex justify-content-between">
                        <h6><a href="" class="text-decoration-none text-light-blue">{{ i.title }}</a></h6>
                        <span class="text-white">%{{ i.percent }}</span>
                    </div>
                    <div class="progress" style="height: 5px" role="progressbar" aria-label="Warning striped example" :aria-valuenow="i.percent" aria-valuemin="0" aria-valuemax="100">
                        <div class="progress-bar progress-bar-striped bg-success" :style="'width: '+i.percent+'%'"></div>
                    </div>
                    <hr>
                    <p>{{ i.text }}</p>
                </div>
            </div>

        </div>
</template>

<script setup>
import {toRef} from "vue";
import ColoredTitle from "../global/ColoredTitle";

const props = defineProps(['items'])
const items = toRef(props, 'items')
</script>

<style scoped>
.technologyItem p{
    font-size: 16px;
    line-height: 25px;
    height: 75px;
    overflow: hidden;
}
</style>
