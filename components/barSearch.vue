<template>
    <div class="container-search">
        <el-row>
            <el-col :span="8">
                <div class="title-city">   
                    <h1>VILLA PEPITA</h1>
                    <h3> <span>ID </span> 000000000 </h3>
                </div>
            </el-col>

            <el-col :span="16">
                <div class="select-container">
                    <div>
                        <customSelect :title="'PREDIO'" :icon="'fas fa-map-marker-alt'" :data="predios" />
                    </div>

                    <div>
                        <customSelect :title="'CULTIVO'" :icon="'fab fa-pagelines'" :data="cultivos" />
                    </div>

                    <div>
                        <customSelect :title="'LOTE'" :icon="'fas fa-spa'" :data="lotes" />
                    </div>

                    <div>
                        <el-input class="search-input" placeholder="Buscar" suffix-icon="fas fa-microphone" prefix-icon="fas fa-search" v-model="search">
                        </el-input>
                    </div>
                </div>
            </el-col>
        </el-row>
    </div>
</template>

<script>
import customSelect from '@/components/customSelect';

export default {
    components: {
        customSelect
    },
    data () {
        return {
            lote: '',
            cultivo: '',
            search :'',
            predios: [
                {
                    value: 'Option1',
                    label: 'Option1'
                }, {
                    value: 'Option2',
                    label: 'Option2'
                }
            ],
            cultivos: [
                {
                    value: 'Option1',
                    label: 'Option1'
                }, {
                    value: 'Option2',
                    label: 'Option2'
                }
            ],
            lotes: [
                {
                    value: 'Option1',
                    label: 'Option1'
                }, {
                    value: 'Option2',
                    label: 'Option2'
                }
            ]
        }
    }
}
</script>

<style>
    .container-search {
        margin: 15px auto;
    }

    .title-city h1 {
        margin: 0px;
        color: #0B3842;
    }

    .title-city h3 {
        margin: 0px;
        color: #0B3842;
    }

    .title-city h3 span { 
        color: #797474;
        font-weight: normal;
    }

    .select-container {
        display: grid;
        grid-template-columns: 2fr 2fr 2fr 5fr;
    }

    .search-input {
        font-size: 18px;
    }

    .search-input input {
        height: 30px;
        font-family: 'Open Sans';
        background-color: #EDEDEE;

        color: #888 !important;
    }
</style>