<template>
  <div class="wrapper">
    <div class="section page-header header-filter" :style="headerStyle">
      <div class="container">
        <div class="md-layout">
          <div
            class="md-layout-item md-size-33 md-small-size-66 md-xsmall-size-100 md-medium-size-40 mx-auto"
          >
            <login-card header-color="green">
              <h4 slot="title" class="card-title">Web Panel </h4>
              <md-button   href="https://www.facebook.com/resclicksoft/"
                target="_blank"
                slot="buttons"
                class="md-just-icon md-simple md-white"
              >
                <i class="fab fa-facebook-square"></i>
              </md-button>
              <md-button
              href="https://twitter.com/ResClick"
                target="_blank"
                slot="buttons"
                class="md-just-icon md-simple md-white"
              >
                <i class="fab fa-twitter"></i>
              </md-button>
              <md-button
              href="https://www.instagram.com/resclicksoft/"
                target="_blank"
                slot="buttons"
                class="md-just-icon md-simple md-white"
              >
                <i class="fab fa-instagram"></i>
              </md-button>
              <p slot="description" class="description">ResClick</p>
              
              <md-field class="md-form-group" slot="inputs">
                <md-icon>email</md-icon>
                <label>Email</label>
                <md-input v-model="email" type="email"></md-input>
              </md-field>
              <md-field class="md-form-group" slot="inputs">
                <md-icon>lock_outline</md-icon>
                <label>Şifre</label>
                <md-input v-model="password" type="password"></md-input>
              </md-field>
              <md-button slot="footer" class="md-simple md-success md-lg">
                Giriş Yap
              </md-button>
            </login-card>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { LoginCard } from "@/components";

export default {
  components: {
    LoginCard
  },
  bodyClass: "login-page",
  data() {
    return {
      firstname: null,
      email: null,
      password: null
    };
  },
  props: {
    header: {
      type: String,
      default: require("@/assets/img/res-bg.jpg")
    }
  },
  computed: {
    headerStyle() {
      return {
        backgroundImage: `url(${this.header})`
      };
    }
  }
};
</script>

<style lang="css">
.section.page-header.header-filter{
  background-size: cover;
  background-position: center;
}
</style>
