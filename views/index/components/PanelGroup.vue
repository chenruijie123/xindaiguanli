<template>
  <el-row :gutter="40" class="panel-group">
    <el-col :xs="12" :sm="12" :lg="6" class="card-panel-col" v-for="item in data" :key="item.id">
      <div class="card-panel">
        <div class="card-panel-icon-wrapper">
          <svg-icon :icon-class='iconClass' :class-name="className" />
        </div>
        <div class="card-panel-description">
          <div class="card-panel-text">
            {{item.text}}
          </div>
          <div class="card-panel-num">{{item.num}}</div>
        </div>
      </div>
    </el-col>
  </el-row>
</template>

<script>
export default {
  props:{
    iconClass: {
      type: String,
      default: 'money'
    },
    className: {
      type: String,
      default: 'card-money-icon'
    },
    data: {
      type: Array,
      default: ''
    }
  },
  methods: {
   
  }
}
</script>

<style lang="scss" scoped>
.panel-group {
  margin-top: 18px;

  .card-panel-col {
    margin-bottom: 32px;
  }

  .card-panel {
    height: 108px;
    cursor: pointer;
    font-size: 12px;
    position: relative;
    overflow: hidden;
    color: #666;
    background: #fff;
    box-shadow: 4px 4px 40px rgba(0, 0, 0, .05);
    border-color: rgba(0, 0, 0, .05);
    &:hover {
      .card-panel-icon-wrapper {
        color: #fff;
      }
      .icon-money {
        background: #f4516c;
      }
    }
    .icon-money {
      color: #f4516c;
    }
    .card-panel-icon-wrapper {
      float: left;
      margin: 14px 0 0 14px;
      padding: 16px;
      transition: all 0.38s ease-out;
      border-radius: 10px;
    }
    .card-money-icon {
      float: left;
      font-size: 48px;
      color:red
    }
    .card-edit-icon {
      float: left;
      font-size: 48px;
      color:blue
    }
    .card-panel-description {
      float: right;
      font-weight: bold;
      margin: 26px;
      margin-left: 0px;

      .card-panel-text {
        line-height: 18px;
        color: rgba(0, 0, 0, 0.45);
        font-size: 16px;
        margin-bottom: 12px;
      }
      .card-panel-num {
        font-size: 20px;
      }
    }
  }
}
@media (max-width:550px) {
  .card-panel-description {
    display: none;
  }
  .card-panel-icon-wrapper {
    float: none !important;
    width: 100%;
    height: 100%;
    margin: 0 !important;
    .svg-icon {
      display: block;
      margin: 14px auto !important;
      float: none !important;
    }
  }
}
</style>
