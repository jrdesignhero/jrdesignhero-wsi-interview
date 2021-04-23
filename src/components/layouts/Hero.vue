<template>
  <div className="reset">
    <div id="quick-view" :className="modalStateClassName">
      <div id="modal-title">
        <h1>Quick Purchase</h1>
      </div>
      <span id="close" v-on:click="toggleModal">CLOSE X</span>

      <div className="reset">
        <div
          v-for="product in apiProducts.slice(0, 4)"
          :key="product"
          className="product-item f-left"
        >
          <img className="w100" :src="product.leaderSkuImage" />
          <h6 className="product-title">
            {{ product.title }}
          </h6>
          <ul>
            <li>
              <span className="labelProduct">Sale Price: </span>
              <span className="productResult">${{ product.sale_price }}</span>
            </li>
          </ul>
          <a
            className="buyNowBtn"
            href="https://www.williams-sonoma.com/shop/cookware/anolon-x-cookware/?cm_re=hphero-_-default-_-shop_anolonx&isx=0.0.0"
            >Buy Now</a
          >
        </div>
      </div>

      <a href="#" id="seeMore">View All ></a>
    </div>
    <div
      id="quick-view-bg"
      v-on:click="toggleModal"
      :className="modalStateClassName"
    ></div>
    <img v-on:click="toggleModal" className="w100" :src="img" />
  </div>
</template>

<script>
export default {
  name: "Hero",
  props: {
    img: String,
  },
  data() {
    return {
      modalState: 0,
      modalStateClassName: "d-none",
      apiProducts: "",
    };
  },
  methods: {
    getQuickBuy: function (vm) {
      fetch(
        "https://core.dxpapi.com/api/v1/core/?q=anolon-x-cookware&start=0&rows=20&request_type=search&search_type=category&request_id=827014793835&_br_uid_2=uid=7974570928334:v=12.0:ts=1619047558491:hc=25&account_id=4060&url=https://www.williams-sonoma.com/&domain_key=williamssonoma_en_ws_prd_d1&fq=inactive%3A%22false%22&fq=availability_logic%3A%22true%22&fl=pid%2Cprice%2Cprice_range%2Csale_price%2Csale_price_range%2Cthumb_image%2Ctitle%2CeligibleForQuickBuy%2CpipThumbnailMessages%2Cflags%2CisBopisOnly%2CimageOverride%2CaltImages%2Cstore_ids%2Ccategory_name_attr%2Ccategory_id_attr%2CpageLoadImages%2CimageRollOvers%2ChoverImages%2Cthumb_image_attr%2CleaderSkuImage%2CswatchesDisplay%2CmoreSwatchesCount%2CproductPriceType%2CmaxDiscountPercent&efq=ship_to_store_ids:(%22ST%3A0795%22%20OR%20%22ST%3A0413%22%20OR%20%22ST%3A0814%22%20OR%20%22ST%3A6073%22%20OR%20%22ST%3A0726%22%20OR%20%22ST%3A6049%22%20OR%20%22ST%3A0011%22%20OR%20%22ST%3A0308%22%20OR%20%22ST%3A0021%22%20OR%20%22ST%3A0218%22%20OR%20%22ST%3A0618%22%20OR%20%22ST%3A0848%22%20OR%20%22ST%3A6134%22%20OR%20%22ST%3A0856%22%20OR%20%22ST%3A0625%22%20OR%20%22ST%3A0945%22)%20OR%20store_ids:(%22ST%3A0795%22%20OR%20%22ST%3A0413%22%20OR%20%22ST%3A0814%22%20OR%20%22ST%3A6073%22%20OR%20%22ST%3A0726%22%20OR%20%22ST%3A6049%22%20OR%20%22ST%3A0011%22%20OR%20%22ST%3A0308%22%20OR%20%22ST%3A0021%22%20OR%20%22ST%3A0218%22%20OR%20%22ST%3A0618%22%20OR%20%22ST%3A0848%22%20OR%20%22ST%3A6134%22%20OR%20%22ST%3A0856%22%20OR%20%22ST%3A0625%22%20OR%20%22ST%3A0945%22)%20OR%20fulfillment_locations:(%22LAXDTC%22%20OR%20%22COI_CMO%22%20OR%20%22COI_SS%22%20OR%20%22DEFAULT%22)"
      )
        .then((response) => response.json())
        .then(function (data) {
          vm.apiProducts = data.response.docs;
          console.log(vm.apiProducts);
        });
    },
    setModalState: function (state) {
      this.modalState = state;
    },
    showModal: function () {
      this.modalStateClassName = "";
    },
    hideModal: function () {
      this.modalStateClassName = "d-none";
    },
    toggleModal: function () {
      if (this.modalState === 0) {
        this.getQuickBuy(this);
        this.showModal();
        this.setModalState(1);
        return true;
      }
      if (this.modalState === 1) {
        this.hideModal();
        this.setModalState(0);
        return true;
      }
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.reset {
  position: relative;
  overflow: hidden;
}
.d-none {
  display: none;
}
li {
  list-style: none;
}
#close {
  position: absolute;
  top: 0px;
  right: 0px;
  width: 90px;
  background: #000;
  color: #fff;
  text-align: center;
  padding: 5px;
}
h1 {
  font-size: 22px;
  margin-bottom: 10px;
  margin-top: 0px;
  line-height: 24px;
}
#quick-view {
  z-index: 100;
  background: #fff;
  position: absolute;
  width: 600px;
  border-radius: 5px;
  left: 50%;
  margin-left: -320px;
  margin-top: 50px;
  padding: 15px 20px 0px 20px;
  overflow: hidden;
}
#quick-view-bg {
  position: absolute;
  z-index: 99;
  top: 0px;
  bottom: 0px;
  left: 0px;
  right: 0px;
  background: rgba(0, 0, 0, 0.8);
}
.product-item {
  width: 140px;
  margin: 5px;
}
h6.product-title {
  font-size: 12px;
  margin: 7px 0px 3px 0px;
  min-height: 52px;
}
span.labelProduct {
  font-size: 13px;
  width: 65px;
  display: inline-block;
}
#seeMore {
  text-align: center;
  font-size: 20px;
  padding: 7px;
  margin-top: 20px;
  text-decoration: none;
  display: block;
  margin-left: -20px;
  margin-right: -20px;
  padding-bottom: 12px;
  background: #e9e9e9;
  color: black;
}
span.productResult {
  font-size: 13px;
}
.buyNowBtn {
  background: #000;
  display: block;
  text-align: center;
  color: #fff;
  font-size: 13px;
  text-decoration: none;
  padding: 5px;
  margin-top: 7px;
}
#close,
.w100 {
  cursor: pointer;
}
@media only screen and (max-width: 896px) {
  #quick-view {
    margin-top: 20px;
  }
}
@media only screen and (max-width: 830px) {
  .product-title {
    display: none;
  }
}
@media only screen and (max-width: 710px) {
  #quick-view {
    margin-left: -150px;
    left: 50%;
    width: 290px;
    height: 469px;
    padding: 10px 5px 0px 5px;
  }
  .reset {
    overflow: visible;
  }
  #seeMore {
    font-size: 15px;
    padding: 6px;
    text-transform: uppercase;
    margin-top: 10px;
  }
  h1 {
    font-size: 17px;
    margin-bottom: 5px;
  }
  #quick-view-bg {
    position: fixed;
    top: 0px;
    left: 0px;
    right: 0px;
    bottom: 0px;
  }
  .product-item {
    width: 134px;
  }
}
</style>