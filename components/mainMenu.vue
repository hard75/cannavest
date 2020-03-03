
<template>
  <div>
    <el-menu class="el-menu-demo" mode="horizontal">

      <el-row>
        <el-col :span="6">
          <i class="fas fa-bars icon-menu"></i>
        </el-col>

        <el-col :span="12">
          <div style="text-align: center;">
            <img src="logo-cannavest.png" alt="logo" />
          </div>
        </el-col>

        <el-col :span="6">
            <div class="account-info">
              <div>
                <span class="username">{{ username }}</span>
              </div>

              <div>
                <img class="profile-img" src="avatar.png" alt="avatar" />
              </div>

              <div>
                <i class="fas fa-sort-down setting-account"></i>
              </div>
            </div>
        </el-col>
      </el-row>

    </el-menu>
  </div>
</template>
<script>
  export default {
    data() {
      return {
        username: 'Pepito'
      };
    }
  }
</script>

<style>
  .icon-menu {
    font-size: 37px;
    color: #FF6010;

    margin-top: 20px;
    margin-left: 10px;

    cursor: pointer;
  }

  .el-menu-demo {
    margin-top: 22px;
    padding-bottom: 20px;

    color: #0B3842;
  }

  .profile-img {
    width: 70px;
    height: 70px;
    border-radius: 50px;

    object-fit: cover;
    object-position: center right;

    margin: 0px 10px; 
  }

  .account-info {
    display: flex;
    align-items: center;
    justify-content: center;
    
    float:right;
  }

  .account-info .setting-account {
    color: #00AB81;
    font-size: 44px;
    margin-bottom: 15px;

    cursor: pointer;
  }

  .account-info .username {
    font-size:20px;
    font-weight:normal;
  }
</style>