<template>
    <div v-if="visibleMenu" class="menu-bar">
        <i @click="closeMenu" style="color:white;font-size:40px;" class="fas fa-times"></i>

        <div class="menu-lateral" style="margin: 20px; margin-top:70px; text-align:left;">
            <el-row>
                <el-col :span="24">
                    <span style="display:inline-block;">
                        <h1>Dashboard</h1>
                    </span>
                </el-col>
            </el-row>

            <el-row>
                <el-col :span="24">
                     <h1>Licencias</h1>

                </el-col>
            </el-row>

            <el-row>
                <el-col :span="24">
                     <h1>Usuarios</h1>

                </el-col>
            </el-row>

            <el-row>
                <el-col :span="24">
                     <h1>Predio</h1>

                </el-col>
            </el-row>
            
            <el-row>
                <el-col :span="24">
                     <h1>Cultivos</h1>

                </el-col>
            </el-row>

             <el-row>
                <el-col :span="24">
                     <h1>Lotes</h1>
                </el-col>
            </el-row>
        </div>
    </div>
</template>

<script>
export default {
    props: [ 'visibleMenu' ],
    methods: {
        closeMenu () {
            this.$emit('closeMainMenu', false);
        }
    }
}
</script>

<style>
    .menu-bar {
        margin: 0px;
        padding: 30px;
        top: 0px;

        height:94vh;
        width: 300px;
        background-color:#FF6010;
        position:fixed;
        z-index:2000;
    }

    .menu-lateral .el-row .el-col h1 {
        color: #fff;
        font-weight: normal;

        font-family: "adobe-clean", sans-serif;

        cursor: pointer;
    }

    .menu-lateral .el-row .el-col hr {
        color: #ffF;
        width: 150px;
    }
</style>