<template>
  <div class="home">
    <div class="top">
      <h1>理财账本</h1>
      <div class="box">
        <div class="main">
          <div class="left">
            <p>我的净资产 (更新时间) <i>+648.00</i></p>
            <h2>10,0100.00</h2>
            <div class="cen">
              <div class="property">
                <p>总资产</p>
                <p class="sun">20,0100.00</p>
              </div>
              <div class="profit">
                <p>总盈亏</p>
                <p class="sun">+328.00</p>
              </div>
            </div>
          </div>
          <div class="right">
            <img src="@/assets/css/1.png" alt="" />
          </div>
        </div>
        <div class="btn">记一笔</div>
      </div>
    </div>
    <div class="center">
      <div class="list" v-for="(item, index) in inform" :key="index">
        <div class="up">
          <p class="left">{{ item.title }}</p>
          <p class="right">{{ item.number }}</p>
        </div>
        <div class="down">
          <p class="left">{{ item.text }}:××××××××</p>
          <p class="right">更新时间:</p>
        </div>
      </div>
    </div>
    <div class="footer">
      <div class="title">
        <img src="@/assets/css/1.png" alt="" />
        <p>余额记账</p>
      </div>
      <div class="title">
        <img src="@/assets/css/1.png" alt="" />
        <p>行情</p>
      </div>
      <div class="title">
        <img src="@/assets/css/1.png" alt="" />
        <p>社区</p>
      </div>
      <div class="title">
        <img src="@/assets/css/1.png" alt="" />
        <p>我</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HomeView",
  data() {
    return {
      inform: [
        {
          title: "银行活期--中国银行",
          number: "+12.70",
          text: "卡号",
        },
        {
          title: "股票--贵州茅台 SH",
          number: "-200.00",
          text: "代号",
        },
        {
          title: "基金--中概互联",
          number: "-100.00",
          text: "代号",
        },
        {
          title: "基金--泸深300",
          number: "+45.00",
          text: "卡号",
        },
        {
          title: "基金--纳斯达克",
          number: "+1.50",
          text: "卡号",
        },
        {
          title: "上海--住房贷款",
          number: "-8000.00",
          text: "卡号",
        },
      ],
    };
  },
};
</script>
<style lang="less">
body {
  margin: 0;
  padding: 0;
  background-color: #f1f3f5;
}
.top {
  width: 100%;
  height: 250px;
  background-color: #fc7555;
  // display: flex;
  // justify-content: center;
  // align-items: center;
  h1 {
    margin: 0;
    text-align: center;
    color: white;
    font-size: 16px;
    padding-top: 50px;
  }
  .box {
    width: 80%;
    height: 190px;
    padding: 0 15px;
    background-color: white;
    margin-top: 10px;
    margin-left: 50%;
    transform: translatex(-50%);
    border-radius: 8px;
    .main {
      display: flex;
      .left {
        flex: 3;
        p {
          font-size: 13px;
          color: #b6b6b6;
          i {
            color: red;
            font-style: normal;
            font-weight: 600;
          }
        }
        h2 {
          margin: 0;
          margin-top: 10px;
          font-size: 26px;
        }
        .cen {
          display: flex;
          .property {
            flex: 1;
          }
          .profit {
            flex: 1;
          }
          .sun {
            font-size: 16px;
            color: black;
            margin-top: 10px;
          }
        }
      }
      .right {
        flex: 1;
        img {
          margin-top: 30px;
        }
      }
    }
    .btn {
      width: 200px;
      height: 30px;
      background-color: #fd6c51;
      color: white;
      border: none;
      border-radius: 20px;
      margin: 0 auto;
      text-align: center;
      line-height: 30px;
    }
  }
}
.center {
  padding: 0 10px;
  margin-top: 40px;
  .list {
    width: 100%;
    height: 60px;
    margin-bottom: 20px;
    background-color: white;
    display: flex;
    flex-wrap: wrap;
    .up {
      width: 100%;
      height: 25px;
      padding: 0 10px;
      margin-top: 5px;
      display: flex;
      p {
        margin: 0;
        font-size: 16px;
      }
      .left {
        flex: 1;
      }
    }
    .down {
      width: 100%;
      height: 25px;
      padding: 0 10px;
      display: flex;
      p {
        margin: 0;
        font-size: 12px;
        color: #b2b2b2;
      }
      .left {
        flex: 1;
      }
      .right {
        margin-right: 30px;
      }
    }
  }
}
.footer {
  width: 100%;
  height: 50px;
  background-color: white;
  display: flex;
  align-items: center;
  justify-content: space-around;
  .title {
    display: flex;
    flex-direction: column;
    align-items: center;
    img {
      width: 20px;
      height: 25px;
    }
    p {
      margin: 0;
      font-size: 12px;
      text-align: center;
    }
  }
}
</style>
