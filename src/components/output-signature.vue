<template>
  <div>
      <section>
        <table cellpadding="0" cellspacing="0" border="0" style=
        "background: none; border-width: 0px; border: 0px; margin: 0; padding: 0;">
        <tr>
            <td valign="top" style="padding-top: 0; padding-bottom: 0; padding-left: 0; padding-right: 7px; border-top: 0; border-bottom: 0; border-left: 0;">
              <a href="https://www.junkluggers.com/">
                <img v-show="mobilePhoneSwitch" width="220" height="139" style="width: 220px; max-width: 220px !important; height: 139px; max-height: 139px !important; margin-top: 5px;" id="preview-image-url" src="https://cdn.treehouseinternetgroup.com/cms_images/2714/junkluggers-output-logo.png" name="preview-image-url" />
        
                <img v-show="!mobilePhoneSwitch" width="180" height="113" style="width: 180px; max-width: 180px !important; height: 113px; max-height: 113px !important; margin-top: 5px;" id="preview-image-url" src="https://cdn.treehouseinternetgroup.com/cms_images/2714/junkluggers-output-logo.png" name="preview-image-url" /> 
              </a>
            </td> 
            
            <td style=
            "padding-top: 0; padding-bottom: 0; padding-left: 5px; padding-right: 0;">
            <table cellpadding="0" cellspacing="0" border="0" style=
            "background: none; border-width: 0px; border: 0px; margin: 0; padding: 0;">
              <tr>
                  <td colspan="2" style=
                  "padding-bottom: 5px; color: #3ad532; font-size: 18px; font-family: Arial, Helvetica, sans-serif;">
                  {{fullName}}
                  </td>
                </tr>
                <tr>
                  <td colspan="2" style=
                  "color: #333333; font-size: 14px; font-family: Arial, Helvetica, sans-serif;">
                  <em>{{title}}</em>
                  </td>
                </tr>
              <div v-show="!mobilePhoneSwitch">

              </div>
             
                <tr>
                  <td width="20" valign="top" style=
                  "vertical-align: top; width: 20px; color: #3ad532; font-size: 14px; font-family: Arial, Helvetica, sans-serif;">
                  p:
                  </td>
                  <td valign="top" style=
                  "vertical-align: top; color: #333333; font-size: 14px; font-family: Arial, Helvetica, sans-serif;">
                  {{phone}}
                  </td>
                </tr>
                <tr v-show="mobilePhoneSwitch">
                <td width="20" valign="top" style=
                  "vertical-align: top; width: 20px; color: #3ad532; font-size: 14px; font-family: Arial, Helvetica, sans-serif;">
                  m:
                  </td>
                  <td valign="top" style=
                  "vertical-align: top; color: #333333; font-size: 14px; font-family: Arial, Helvetica, sans-serif;">
                  {{mobilePhone}}
                  </td>
                </tr>
                <tr>
                    <td width="20" valign="top" style=
                    "vertical-align: top; width: 20px; color: #3ad532; font-size: 14px; font-family: Arial, Helvetica, sans-serif;">
                    e:
                    </td>
                    <td valign="top" style=
                    "vertical-align: top; color: #333333; font-size: 14px; font-family: Arial, Helvetica, sans-serif;">
                    <a :href="`mailto:${this.email}`" style="color: #333333; text-decoration: none; font-weight: normal; font-size: 14px;">{{email}}</a>
                      &nbsp;&nbsp;
                    </td>
                  </tr>
                <tr>
                  <td width="20" valign="top" style=
                  "vertical-align: top; width: 20px; color: #3ad532; font-size: 14px; font-family: Arial, Helvetica, sans-serif;">
                  w:
                  </td>
                  <td valign="top" style=
                  "vertical-align: top; color: #333333; font-size: 14px; font-family: Arial, Helvetica, sans-serif;">
                  <a href="https://www.junkluggers.com/" target="_blank" style=
                  "color: #333333; text-decoration: none; font-weight: normal; font-size: 14px;">
                    junkluggers.com</a>
                    &nbsp;&nbsp;
                  </td>
                </tr>
                <tr>
                    <td width="20" valign="top" style=
                    "vertical-align: top; width: 20px; color: #3ad532; font-size: 14px; font-family: Arial, Helvetica, sans-serif;">
                    a:
                    </td>
                    <td valign="top" style=
                    "vertical-align: top; color: #333333; font-size: 14px; font-family: Arial, Helvetica, sans-serif;">
                    {{address}}
                      &nbsp;&nbsp;
                    </td>
                  </tr>
                                  <tr>
                  <td colspan="2" style="padding-top: 5px;">
                    <a href="https://www.facebook.com/TheJunkluggers/" target="_blank" style=
                    "border-width:0px; border:0px; text-decoration: none;"><img width="25"
                    height="25" style=
                    "border: none; width: 25px; max-width: 25px !important; height: 25px; max-height: 25px !important;"
                    src=
                    "https://cdn.treehouseinternetgroup.com/cms_images/2714/fb-icon.png" /></a>
                    
                    <!-- <a href="https://www.linkedin.com/company/larry-janeskys-healthy-basement-systems" target="_blank" style=
                    "border-width:0px; border:0px; text-decoration: none;"><img width="25"
                    height="25" style=
                    "border: none; width: 25px; max-width: 25px !important; height: 25px; max-height: 25px !important;"
                    src=
                    "https://dc69b531ebf7a086ce97-290115cc0d6de62a29c33db202ae565c.ssl.cf1.rackcdn.com/2822/icon-linkedin_30x30-2.png" /></a> -->
                    
                    <!-- <a href="https://g.page/mid-state-basement-systems-oh/review?rc" target="_blank"
                    style=
                    "border-width:0px; border:0px; text-decoration: none;"><img width="25"
                    height="25" style=
                    "border: none; width: 25px; max-width: 25px !important; height: 25px; max-height: 25px !important;"
                    src=
                    "https://cdn.treehouseinternetgroup.com/cms_images/2726/icon-google_30x30.png" /></a> -->
                    <a href="https://twitter.com/junkluggers" target="_blank"
                    style=
                    "border-width:0px; border:0px; text-decoration: none;"><img width="25"
                    height="25" style=
                    "border: none; width: 25px; max-width: 25px !important; height: 25px; max-height: 25px !important;"
                    src=
                    "https://cdn.treehouseinternetgroup.com/cms_images/2714/twitter-icon.png" /></a>
                    <a href="https://www.instagram.com/thejunkluggers/" target="_blank"
                    style=
                    "border-width:0px; border:0px; text-decoration: none;"><img width="25"
                    height="25" style=
                    "border: none; width: 25px; max-width: 25px !important; height: 25px; max-height: 25px !important;"
                    src=
                    "https://cdn.treehouseinternetgroup.com/cms_images/2714/insta-icon.png" /></a>
                    <a href="https://www.youtube.com/channel/UCjQQKzxNw-0n-xGx90D8sLg" target="_blank"
                    style=
                    "border-width:0px; border:0px; text-decoration: none;"><img width="25"
                    height="25" style=
                    "border: none; width: 25px; max-width: 25px !important; height: 25px; max-height: 25px !important;"
                    src=
                    "https://cdn.treehouseinternetgroup.com/cms_images/2714/yt-icon.png" /></a>
                    <!-- <a href="https://www.tiktok.com/@healthybasementsystems?lang=en" target="_blank"
                    style=
                    "border-width:0px; border:0px; text-decoration: none;"><img width="25"
                    height="25" style=
                    "border: none; width: 25px; max-width: 25px !important; height: 25px; max-height: 25px !important;"
                    src=
                    "https://cdn.treehouseinternetgroup.com/cms_images/48/tiktok-icon.png" /></a> -->
                  </td>
                </tr>
              </table>
            </td>
          </tr>
        </table>
        <p style="font-size: 10px; color: #000; line-height: 12px;text-align: left; width: 450px" width="450">This message contains confidential information and is intended only for the intended recipients. If you are not an intended recipient you should not disseminate, distribute or copy this e-mail. Please notify us immediately by e-mail if you have received this e-mail by mistake and delete this e-mail from your system. E-mail transmission cannot be guaranteed to be secure or error-free as information could be intercepted, corrupted, lost, destroyed, arrive late or incomplete, or contain viruses. Therefore we do not accept liability for any errors or omissions in the contents of this message, which arise as a result of e-mail transmission. If verification is required please request a hard-copy version.</p>
    </section>
  </div>
</template>
<script>
export default {
  name: 'outputSignature',
  props: {
    fullName: {
      type: String,
      required: true
    },
    title: {
      type: String,
      required: true
    },
    mobilePhone: {
      type: String,
      required: true
    },
    phone: {
      type: String,
      required: true
    },
    email: {
      type: String,
      required: true
    },
    address: {
      type: String,
      required: true
    },
    mobilePhoneSwitch: {
      type: Boolean,
      required: true
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #3ad532;
}
</style>
