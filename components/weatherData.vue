<template>
    <el-row class="weather-data">
        <el-col :span="7">
            <div class="title-weather">
                <span>Condiciones climáticas</span>
            </div>
            <div class="conditions">
                <div>
                    <img src="temperatura/22temp.png" alt="22" />
                </div>
                <div>
                    <img src="temperatura/70temp.png" alt="70" />
                </div>
                <div>
                    <img src="temperatura/25temp.png" alt="25" />
                </div>
                <div>
                    <img src="temperatura/30temp.png" alt="30" />
                </div>
            </div>
        </el-col>
        <el-col :span="10">
            <div class="title-weather">
                <span>Km3 vereda pepito</span>
            </div>
            <div style="text-align:center;">
                <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d5623.783096275368!2d-74.09614297067122!3d4.662510273806196!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x8e3f28eb1616af2b%3A0x933cbcb5fad108ed!2sCundinamarca!5e0!3m2!1ses-419!2sco!4v1583240275511!5m2!1ses-419!2sco" 
                    width="700" 
                    height="450" 
                    frameborder="0" 
                    style="border-radius:12px; position: relative; margin:auto;"
                    allowfullscreen="">
                </iframe>
            </div>
        </el-col>

        <el-col :span="7">
             <div class="numbers">
                <div style="border-top-left-radius: 12px;">
                    <span class="subtitle">Número de lotes en producción</span><br>
                    <span class="title">07</span>
                </div>
                <div style="border-top-right-radius: 12px;">
                    <span class="subtitle">Número de lotes en producción activos</span><br>
                    <span class="title">06</span>
                </div>
                <div style="border-bottom-left-radius: 12px;">
                    <span class="subtitle">Trabajadores asociados</span>
                    <span class="title">02</span>
                </div>
                <div style="border-bottom-left-radius: 12px;">
                    <span class="subtitle">Número de cultivos</span>
                    <span class="title">03</span>
                </div>
            </div>
        </el-col>
    </el-row>
</template>

<script>
export default {
    mounted () {
       
    }   
}
</script>

<style>
    .weather-data {
        margin-top: 60px;
    }

    .conditions {
        display: grid;

        grid-template-rows: 2fr 2fr;
        grid-template-columns: 2fr 2fr;
    }

    .conditions div {
        margin: 20px;
    }

    .title-weather {
        text-align: center;
        width: 100%;
        margin: 20px;

        font-size: 22px;
    }

    #googleMap {
        width:100%;
        height:300px;
        border-radius:12px;

        margin-right: 20px;
    }

    .numbers {
        margin: 20px;
        text-align: center;
        margin-top: 70px;

        display: grid;

        grid-template-rows: 4fr 4fr;
        grid-template-columns: 3fr 3fr;
    }

    .numbers div {
        background-color: #EDEBE8;
        padding: 20px;

        display: block;

        margin: 1px;
        padding-top: 30px;
        padding-bottom: 30px;
    }

    .numbers div .title {
        font-size: 100px;
        font-weight: bold;

        margin: 10px;

    }

    .numbers div .subtitle {
        font-size: 15px;
        margin: 10px;
    }
</style>