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
              </table>
            </td>
          </tr>
        </table>
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
