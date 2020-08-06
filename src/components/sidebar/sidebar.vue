<template>
  <div class="sidebar">
    <div class="sidebar-header">
      <div class="tips">
        <i class="iconfont icon-tixing"></i>
        <div class="dot"></div>
      </div>
      <div class="avatar">
        <div class="name">Anastasia</div>
        <div class="img">
          <img
            src="https://img.bosszhipin.com/beijin/mcs/useravatar/20181216/b0f444e71d8d24b730d386e1f14d25a45d9664eee9ab31f2a472548625a523d9_s.png"
            alt="avatar"
          />
        </div>
      </div>
    </div>
    <div id="charts2"></div>
    <div class="section">
      <div class="section-title">
        <div>Transactions</div>
        <div>Today ∨</div>
      </div>
      <div class="section-item">
        <div class="icon">
          <i class="iconfont icon-lanqiu"></i>
        </div>
        <div>Dribbble Pro Plan</div>
        <div class="negative">-$100</div>
      </div>
      <div class="section-item">
        <div class="icon">
          <i class="iconfont icon-idea"></i>
        </div>
        <div>Adidas Refund</div>
        <div class="positive">+$230</div>
      </div>
      <div class="section-item">
        <div class="icon">
          <i class="iconfont icon-V"></i>
        </div>
        <div>Wacom LCD</div>
        <div class="negative">-$3000</div>
      </div>
    </div>
    <div class="transfer">
      <div>Transfer Money</div>
      <i class="iconfont icon-youjiantouxiangyouxianxing"></i>
    </div>
    <div class="message">
      <i class="iconfont icon-xinxi"></i>
    </div>
  </div>
</template>
<script>
export default {
  name: "sidebar",
  mounted() {
    var myChart2 = this.$echarts.init(document.getElementById("charts2"));
    // 绘制图表
    myChart2.setOption({
      tooltip: {
        trigger: "item",
        formatter: "{a} <br/>{b}: {c} ({d}%)",
      },
      legend: {
        show: false,
      },
      series: [
        {
          name: "访问来源",
          type: "pie",
          radius: ["50%", "70%"],
          avoidLabelOverlap: false,
          label: {
            show: false,
            position: "center",
          },
          emphasis: {
            label: {
              show: true,
              fontSize: "30",
              fontWeight: "bold",
            },
          },
          labelLine: {
            show: false,
          },
          data: [
            { value: 335, name: "嘻嘻嘻" },
            { value: 310, name: "哈哈哈" },
            { value: 234, name: "哦哦哦" },
          ],
        },
      ],
    });
  },
};
</script>
<style lang="scss" scoped>
.sidebar {
  position: relative;
  border-radius: 50px 0 0 50px;
  box-shadow: -6px -4px 11px #eae8e8;
  & #charts2 {
    margin-left: auto;
    margin-right: auto;
    height: 300px;
    width: 300px;
  }
  & .sidebar-header {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    width: 90%;
    margin-left: auto;
    margin-right: auto;
    margin-top: 30px;
    & .tips {
      position: relative;
      & i {
        font-size: 35px;
      }
      & .dot {
        position: absolute;
        right: 5px;
        top: 5px;
        width: 10px;
        height: 10px;
        background-color: red;
        border-radius: 50%;
      }
    }
    & .avatar {
      display: flex;
      align-items: center;
      & .name {
        font-weight: bold;
      }
      & .img {
        width: 40px;
        height: 40px;
        margin-left: 10px;
        border-radius: 50%;
        overflow: hidden;
        & img {
          width: 100%;
          height: 100%;
        }
      }
    }
  }
  & .section {
    width: 90%;
    margin-left: auto;
    margin-right: auto;
    & .section-title {
      display: flex;
      justify-content: space-between;
      color: #b4b4b4;
    }
    & .section-item {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-top: 30px;
      font-weight: bold;
      & .icon,
      .negative {
        color: $redColor;
      }
      & .icon {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 50px;
        height: 50px;
        box-shadow: 1px 1px 10px #eae8e8;
        & .iconfont {
          font-size: 30px;
        }
      }
      & .positive {
        color: #1d88a0;
      }
    }
  }
  & .transfer {
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 50px;
    width: 70%;
    margin-left: auto;
    margin-right: auto;
    margin-top: 40px;
    padding: 0 20px;
    border-radius: 30px;
    background-color: $redColor;
    color: #f7f7f7;

  }
  & .message {
    display: flex;
    justify-content: center;
    align-items: center;
    position: absolute;
    right: 20px;
    bottom: 20px;
    width: 50px;
    height: 50px;
    border-radius: 50%;
    box-shadow: 1px 1px 10px #1d88a0;
    background-color: #1d88a0;
    & .iconfont {
      color: #f7f7f7;
      font-size: 30px;
    }
  }
}
</style>