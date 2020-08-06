<template>
  <div>
    <div class="item card">
      <div class="item-header">
        <div class="title">Cards</div>
        <div class="view">View all cards</div>
      </div>
      <div class="item-content">
        <div class="card-item">
          <div class="bottom-card">
            <div class="card-title">Avaliable balance</div>
            <div class="card-number">
              ****
              <span></span>****
              <span></span>****
              <span></span>**34
            </div>
          </div>
          <div class="top-card">
            <div class="money">$ 2,200</div>
            <div class="name">Monzo</div>
            <div class="icon">
              <div class="red"></div>
              <div class="yellow"></div>
            </div>
          </div>
        </div>
        <div class="card-item">
          <div class="bottom-card">
            <div class="card-title">Avaliable balance</div>
            <div class="card-number">
              ****
              <span></span>****
              <span></span>****
              <span></span>**67
            </div>
          </div>
          <div class="top-card green">
            <div class="money">$ 1,300.89</div>
            <div class="name">Monzo</div>
            <div class="icon">
              <div class="red"></div>
              <div class="yellow"></div>
            </div>
          </div>
        </div>
        <div class="card-item">
          <div class="bottom-card">
            <div class="wrapper">
              <div class="icon">
                <i class="iconfont icon-addTodo-nav"></i>
              </div>
              <div class="text">Add New Card</div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="main">
      <div class="left">
        <div class="item">
          <div class="item-header">
            <div class="title">Main Services</div>
            <div class="view">View all</div>
          </div>
          <div class="item-contnt">
            <div class="services-item">
              <i class="iconfont icon-transfer"></i>
              <div>transactions</div>
            </div>
            <div class="services-item">
              <i class="iconfont icon-idea"></i>
              <div>Utililty</div>
            </div>
            <div class="services-item">
              <i class="iconfont icon-jineqiandaiyueshangjin"></i>
              <div>loans</div>
            </div>
            <div class="services-item">
              <i class="iconfont icon-qianbaoqiandaiyue"></i>
              <div>Deposits</div>
            </div>
            <div class="services-item">
              <i class="iconfont icon-transfer"></i>
              <div>Fast transfer</div>
            </div>
            <div class="services-item">
              <i class="iconfont icon-exchange"></i>
              <div>Exchange</div>
            </div>
          </div>
        </div>
      </div>
      <div class="right">
        <div class="top">
          <div class="item">
            <div class="item-header">
              <div class="title">Current</div>
              <div class="view">View all</div>
            </div>
            <div class="item-contnt">
              <div class="item-wrapper">
                <div class="number-item">1063873637834</div>
                <div class="line"></div>
                <div class="money--item">$ 2,200.01</div>
              </div>
              <div class="item-wrapper">
                <div class="number-item">1063873637834</div>
                <div class="line"></div>
                <div class="money--item">$ 2,200.01</div>
              </div>
              <div class="item-wrapper">
                <div class="number-item">1063873637834</div>
                <div class="line"></div>
                <div class="money--item">$ 2,200.01</div>
              </div>
            </div>
          </div>
        </div>
        <div class="bottom">
          <div class="item">
            <div class="item-header">
              <div class="title">Savings</div>
              <div class="view">View all</div>
            </div>
            <div class="item-contnt">
              <div id="charts"></div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "dashboar",
  mounted(){
    // 基于准备好的dom，初始化echarts实例
var myChart = this.$echarts.init(document.getElementById('charts'));
// 绘制图表
myChart.setOption({
    xAxis: {
        type: 'category',
        axisLine: {
      show: false,
      onZero: true
    },
    axisTick: {
      show: false
    },
        data: ['Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat', 'Sun']
    },
    yAxis: {
        type: 'value',
          axisLine: {
      show: false
    },
    axisTick: {
      show: false
    },
    splitLine: {
      lineStyle: {
        type: "dashed"
      }
    }
    },
    series: [{
        data: [820, 932, 901, 934, 1290, 1330, 1320],
        type: 'line',
        smooth: true
    }]
});
  }
};
</script>
<style lang="scss" scoped>
.item {
  margin-top: 20px;
  margin-bottom: 20px;
  width: 100%;
  & .item-header {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    & .title {
      font-size: 20px;
      font-weight: bold;
    }
    & .view {
      color: #b4b4b4;
    }
  }
  & .item-content {
    margin: 20px 0 40px;
  }
}
.card {
  & .item-content {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    & .card-item {
      position: relative;
      height: 200px;
      width: 33%;
      border-radius: 25px;
      overflow: hidden;
      & .top-card,
      .bottom-card {
        position: relative;
        width: 100%;
        height: 100%;
        margin-left: 10px;
        border-radius: 25px;
        & .wrapper {
          display: flex;
          flex-direction: column;
          align-items: center;
          justify-content: center;
          position: absolute;
          width: 40%;
          height: 40%;
          left: 30%;
          top: 30%;
          overflow: hidden;
          color: #b4b4b4;
          & .icon {
            width: 40px;
            height: 40px;
            border: 1px dashed #e6e2e2;
            border-radius: 50%;
            text-align: center;
            line-height: 40px;
            cursor: pointer;
            & .icon-addTodo-nav {
              font-size: 20px;
              font-weight: bold;
              color: #e6e2e2;
            }
          }
          & .text {
            margin-top: 10px;
            font-size: 12px;
          }
        }
      }
      & .bottom-card {
        background-color: #f8f8f8;
        & .card-title {
          font-size: 14px;
          margin: 20px 0 0 40px;
        }
        & .card-number {
          font-size: 18px;
          font-weight: bold;
          margin: 60px 0 0 40px;
          & span {
            display: inline-block;
            width: 20px;
          }
        }
      }
      & .top-card {
        position: absolute;
        top: 0;
        left: 0;
        background: rgba($color: $redColor, $alpha: 0.8);
        & .money {
          margin: 40px 0 0 40px;
          color: #fff;
          font-size: 18px;
          font-weight: bold;
        }
        & .name {
          display: inline-block;
          margin: 80px 0 0 40px;
          color: #fff;
          font-size: 18px;
          font-weight: bold;
        }
        & .icon {
          display: inline-block;
          position: absolute;
          top: 140px;
          right: 50px;
          & .red,
          .yellow {
            border-radius: 50%;
            width: 30px;
            height: 30px;
          }
          & .red {
            background-color: $redColor;
          }
          & .yellow {
            position: absolute;
            top: 0;
            right: -20px;
            background-color: yellow;
          }
        }
      }
      & .green {
        background: rgba($color: #0e809a, $alpha: 0.8);
      }
    }
  }
}
.main {
  display: flex;
  justify-content: space-between;
  & .left {
    width: 35%;
    & .item-contnt {
      display: flex;
      flex-direction: row;
      flex-wrap: wrap;
      justify-content: center;
      & .services-item {
        width: 40%;
        height: 150px;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        margin: 20px 0 0 20px;
        border: 2px solid #fff;
        border-radius: 20px;
        box-shadow: 8px 8px 16px #f7f7f7;
        & .iconfont {
          display: flex;
          justify-content: center;
          align-items: center;
          font-size: 35px;
          color: $redColor;
          height: 60%;
        }
        & div {
          font-size: 14px;
          height: 20%;
          display: flex;
          justify-content: center;
          align-items: center;
        }
      }
    }
  }
  & .right {
    width: 60%;
    & .top {
      .item-contnt {
        margin:20px 0 ;
        width: 100%;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        align-items: center;
        & .item-wrapper {
          margin-top: 10px;
          display: flex;
          width: 100%;
          flex-direction: row;
          justify-content: space-between;
          // align-items: center;
        & .number-item {
          color: #b4b4b4;
          font-weight: bold;
        }
        & .line {
          width: 60%;
          border-bottom: 1px dashed #eee;
        }
        & .money-item {
          font-weight: bold;
        }
        }
      }
    }
    #charts {
      width: 100%;
      height: 400px;
    }
  }
}
</style>