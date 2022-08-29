<template>
  <div id="app"> 
  
    <section class="hero is-primary">
      <div class="hero-body">
        <div class="container">
          <div class="th-logo has-text-centered">
            <img src="https://cdn.treehouseinternetgroup.com/cms_images/2714/JL%20full%20logo_RGB_no-tagline.png" alt="" style="width:250px">
          </div>
        <h1 class="sub-text title has-text-centered">
            <p>Signature Generator</p> 
        </h1>
        </div>
      </div> 
    </section>
<!----------------- Header Ends ---------------->
    <div class="container main">  
      <div>  
        <div class="columns">
<!----------------- Input Information ---------------->  
          <div class="column" id="input-info">
              <h3 class="subtitle">Input Information</h3>
               
            <inputInformation :fullName.sync="fullName" :title.sync="title" :mobilePhone.sync="mobilePhone" :phone.sync="phone" :email.sync="email" :address.sync="address" :mobilePhoneSwitch.sync="mobilePhoneSwitch" v-on:changeTitle="updateTitle($event)" />
<!----------------- Button ---------------->   
    <button v-show="!mobilePhoneSwitch" @click="toggleShow, $modal.show('output')" class="button is-success" type="submit" :disabled="!isValid">
        Copy Signature
    </button>
 
    <button v-show="mobilePhoneSwitch" @click="toggleShow, $modal.show('output')" class="button is-success" type="submit" :disabled="!isValidAss">
        Copy Signature
    </button>

    <button @click.prevent="reset" class="button is-success" type="submit" :disabled="!isReset">
        Reset
    </button>
  </div>
<!----------------- Output Signature ---------------->       
          <div class="column">
              <h3 class="subtitle">Output Signature</h3>
            <outputSignature :fullName.sync="fullName" :title.sync="title" :mobilePhone.sync="mobilePhone" :phone.sync="phone" :email.sync="email" :address.sync="address" :mobilePhoneSwitch.sync="mobilePhoneSwitch" v-on:changeTitle="updateTitle($event)"/>
          </div>
        </div>
      </div>
 <!----------------- Modal ---------------->    
 
        <modal name="output" :height="500">
         
          <div class="sign-box level-item has-text-centered">
              <div class="output-btn">
                  <p class="field">
                      <a class="button is-small" @click="$modal.hide('output')">
                        <span class="icon is-small">
                          <i class="fa fa-times"></i>
                        </span>
                      </a>
                    </p> 
                </div>
            <outputSignature :fullName.sync="fullName" :title.sync="title" :mobilePhone.sync="mobilePhone" :phone.sync="phone" :email.sync="email" :address.sync="address" :mobilePhoneSwitch.sync="mobilePhoneSwitch" v-on:changeTitle="updateTitle($event)"/>
           
          </div>

          <div class="gif-box level-item has-text-centered">
            <ul>
              <li>1. Place cursor at the top-left corner of company logo and click & drag to address line in bottom-right corner</li>
              <li>2. Paste into Outlook signatures in preferences panel</li>
              <li>3. Adjust logo size if needed</li>
            </ul>
          <img src="http://d6449bb3dc657045bfc9-290115cc0d6de62a29c33db202ae565c.r80.cf1.rackcdn.com/687/sign-copy3.gif" alt="">
        </div>
          </modal>
    </div>
  
<!----------------- Footer ---------------->
    <footer class="" id="footer">
        <div class="container">
            <div class="content has-text-centered">
                <p>
                    &copy; 2022 The Junkluggers
                </p>
            </div>
        </div>
    </footer>
  </div>
</template>

<!-------------------------- Scripts ---------------------------->

<script>
export default {
  name: 'app',
  data: function () {
    return {
      fullName: 'Full Name',
      title: 'Title',
      mobilePhone: 'Mobile',
      phone: 'Office',
      email: 'Email',
      address: 'Address',
      isShowing: false,
      mobilePhoneSwitch: false
    }
  },
  computed: {
    isValid: function () {
      return this.fullName !== 'Full Name' && this.title !== 'Title' && this.phone !== 'Office' && this.email !== 'Email' && this.address !== 'Address'
    },
    isValidAss: function () {
      return this.fullName !== 'Full Name' && this.title !== 'Title' && this.mobilePhone !== 'Mobile' && this.phone !== 'Office' && this.email !== 'Email' && this.address !== 'Address'
    },
    isReset: function () {
      return this.fullName !== 'Full Name' || this.title !== 'Title' || this.mobilePhone !== 'Mobile' || this.phone !== 'Office' || this.email !== 'Email' || this.address !== 'Address'
    }
  },
  methods: {
    toggleShow () {
      this.isShowing = !this.isShowing
    },
    show () {
      this.$modal.show('output')
    },
    hide () {
      this.$modal.hide('output')
    },
    reset () {
      this.fullName = 'Full Name'
      this.title = 'Title'
      this.mobilePhone = 'Mobile'
      this.phone = 'Office'
      this.email = 'Email'
      this.address = 'Address'
    },
    updateTitle (updatedTitle) {
      this.mobilePhoneSwitch = updatedTitle
    }
  }
}
</script>

<!-------------------------- Styles ---------------------------->
<style scoped>


li {
  padding-left: 15px; 
  text-indent: -15px;
}

.output-btn {
    right: 0;
    position: absolute;
    top: 0;
    margin-right: 5px;
}
.sign-box {
    margin-top: 30px;
    margin-left: 60px;
}
.gif-box {
  margin-top: 30px;
  margin-left: 1px;
  background-color: #efefef;
  padding: 20px;
  border-top: 1px dashed #3ad532;
}
.gif-box ul {
    text-align:left;
    font-size: 14px;
}
.gif-box p {
   text-align: left;
   padding-right: 20px;
   font-size: 14px;
}
.gif-box img {
   width:250px;
}
.fade-enter-active,
.fade-leave-active {
  -webkit-transition: opacity 0.2s ease-out;
  transition: opacity 0.2s ease-out;
}

.fade-enter,
.fade-leave-to {
  opacity: 0;
}
input:disabled {
    background: #dddddd;
}
.container.main {
  margin-top: 40px;
}
#footer {
    position: fixed;
    left: 0px;
    bottom: 0px;
    height: 45px;
    width: 100%;
    background-color: #efefef;
    padding-top: 10px;
}
#input-info {
  margin-right: 100px;
}
.hero.is-primary {
  background-color: #fff;
  border-bottom: 1px solid #cacaca;
}
.button {
  margin-top: 10px;
}
.button.is-success, .button.is-success[disabled] {
  background-color: #3ad532;
  border-color: transparent;
  color: #fff;
}
.button.is-success.is-hovered,
.button.is-success:hover {
  background-color: #2ee024;
  border-color: transparent;
  color: #fff;
}
.input:focus {
  border-color: #3ad532;
  box-shadow: 0 0 0 0.125em rgba(119, 187, 70, 0.25);
}
.sub-text {
  margin-left: 10px;
  margin-top: 10px;
}
.sub-text p {
  color: #000;
  font-family: "Barlow Condensed", sans-serif;
  font-weight: 700;
  font-size: 24px;
}
.hero-body {
  padding: 1.5rem 1.5rem;
}
.input:focus {
  border-color: #3ad532;
  box-shadow: 0 0 0 0.125em rgba(119, 187, 70, 0.25);
}
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s;
}
.fade-enter,
.fade-leave-to {
  opacity: 0;
}
</style>
