<template>
    <el-card class="box-card tableGraph">
        <el-row>
            <el-col style="margin: 20px;" :span="12">
                  <span class="title">Tabla de producción</span>
                  <el-table
                    :data="tableData"
                    stripe
                    height="400"
                    class="table"
                    style="width: 100%; text-align: center;">
                    <el-table-column
                    prop="lote"
                    label="ID-Lote">
                    </el-table-column>
                    <el-table-column
                    prop="tipo"
                    width="170"
                    label="Tipo de producto">
                    </el-table-column>
                    <el-table-column
                    width="190"
                    label="Progreso">
                      <template slot-scope="scope">
                        <el-progress :percentage="scope.row.progreso" status="success"></el-progress>                        
                      </template>
                    </el-table-column>
                    <el-table-column
                    prop="cantidad"
                    label="Cant">
                    </el-table-column>
                    <el-table-column
                    prop="precio"
                    label="Precio">
                    </el-table-column>
                    <el-table-column
                    prop="total"
                    label="Total">
                    </el-table-column>

                    <el-table-column>
                      <template>
                          <span style="color:#00AB81 !important;font-weight:bold;"> MÁS INFO </span>
                      </template>
                    </el-table-column>
                  </el-table>
            </el-col>

            <el-col style="margin: 20px;" class="graph-data" :span="10">
              <div style="text-align:center;margin-top:50px;" class="title">
                <span style="font-weight:normal;">Producción</span>  LOT-004
              </div>
              <div class="graph" style="margin:20px; margin-top:57px;">
                <canvas id="gas1" width="70" height="30"></canvas>
              </div>
            </el-col>
        </el-row>
    </el-card>
</template>

<script>
  import Chart from 'chart.js';
  export default {
    data() {
      return {
        tableData: [
          {
            lote: 'LOT-001',
            tipo: 'Santa Maria Golden',
            progreso: '70',
            cantidad: '12',
            precio: '45',
            total: 1200
          },
          {
            lote: 'LOT-001',
            tipo: 'Santa Maria Golden',
            progreso: '70',
            cantidad: '12',
            precio: '45',
            total: 1200
          },
          {
            lote: 'LOT-001',
            tipo: 'Santa Maria Golden',
            progreso: '70',
            cantidad: '12',
            precio: '45',
            total: 1200
          },
          {
            lote: 'LOT-001',
            tipo: 'Santa Maria Golden',
            progreso: '70',
            cantidad: '12',
            precio: '45',
            total: 1200
          },
          {
            lote: 'LOT-001',
            tipo: 'Santa Maria Golden',
            progreso: '70',
            cantidad: '12',
            precio: '45',
            total: 1200
          },
          {
            lote: 'LOT-001',
            tipo: 'Santa Maria Golden',
            progreso: '70',
            cantidad: '12',
            precio: '45',
            total: 1200
          },
          {
            lote: 'LOT-001',
            tipo: 'Santa Maria Golden',
            progreso: '70',
            cantidad: '12',
            precio: '45',
            total: 1200
          },
          {
            lote: 'LOT-001',
            tipo: 'Santa Maria Golden',
            progreso: '70',
            cantidad: '12',
            precio: '45',
            total: 1200
          },
          {
            lote: 'LOT-001',
            tipo: 'Santa Maria Golden',
            progreso: '70',
            cantidad: '12',
            precio: '45',
            total: 1200
          }
        ]
      }
    },
    methods: {
      initChart () {
        let ctx = document.getElementById('gas1').getContext('2d');
        let chart = new Chart(ctx, {
            type: 'line',
            data: {
                labels: ['January', 'February', 'March', 'April'],
                datasets: [{
                    label:"NÚMERO DE PLANTAS",
                    fillColor : "#00AB81",
                    strokeColor : "#00AB81",
                    pointColor : "#002B18",
                    pointStrokeColor : "#fff",
                    backgroundColor: "#C7F8DF",
                    data : [20,60,40,30]
                }]
            },
            options: {
                scales: {
                    yAxes: [{
                        ticks: {
                            suggestedMin: 50,
                            suggestedMax: 100
                        }
                    }]
                }
            }
        });
      }
    },
    mounted () {
      this.initChart();
    }
  }
</script>

<style >
  .table-graph {
    margin-top: 20px;
  }

  .tableGraph .el-card__body .el-row .el-col .title {
    font-size: 20px;
    font-weight: bold;

    margin-bottom: 25px;
    margin-left: 27px;
  }

  .tableGraph .el-card__body .el-row .el-col .el-table .el-table__header-wrapper table thead tr th .cell {
    font-weight: normal;
    font-size: 15px;
  }

  .tableGraph .table {
    margin: 20px;
  }

  .tableGraph .el-card__body .el-row .el-col .graph-data {
    display: flex;

    align-items: center;
    justify-content: center;
  }
</style>
