<template>
    <el-row class="databar">
        <el-col class="sections-data" :span="4">
            <img src="bioproduct.png" alt="bio" />
            <span class="line"></span>
        </el-col>

        <el-col  class="city-data" :span="3">
            <span class="subtitle">Ciudad</span><br>
            <span class="title">Cota</span>
            <span style="margin-top: -28px;" class="line"></span>
        </el-col>

        <el-col class="city-data" :span="5">
            <span class="subtitle">Departamento</span><br>
            <span class="title">Cundinamarca</span>
            <span style="margin-top: -28px;" class="line"></span>
        </el-col>

        <el-col class="city-data" :span="3">
            <span class="subtitle">Total licencias</span><br>
            <span class="title">12</span>
            <span style="margin-top: -28px;" class="line"></span>
        </el-col>

        <el-col class="city-data" :span="3">
            <span class="subtitle">Total lotes</span><br>
            <span class="title">36</span>
            <span style="margin-top: -28px;" class="line"></span>
        </el-col>

        <el-col class="city-data" :span="6">
            <div class="subtitle">
                 <span style="margin-right:105px;">Área cultivada</span>
                 <span>Área total</span>
            </div>

            <div class="title">
                 <span style="color:#00AB81;">6834 m<SUP style="color:#00AB81;">2</SUP></span>
                 /
                 <span>9502 m<SUP>2</SUP></span>
            </div>
        </el-col>
    </el-row>
</template>

<script>
export default {
    
}
</script>

<style>
    .databar {
        display: flex;

        align-items: center;
        justify-content: center;
    }

    .databar .sections-data {
        text-align:center;
    }

    .databar .line {
        border-left: 2px solid #868686;
        height: 90px;

        float:right;

        margin-top: 18px;
    }

    .databar .title {
        font-size: 48px;
        font-weight: bold;
    }

    .databar .subtitle {
        font-size: 20px;
    }

    .databar .city-data {
        text-align: center;
    }

     .databar .line span {
         margin-top: 0px;
     }
</style>