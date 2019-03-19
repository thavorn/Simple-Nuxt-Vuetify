<template>
  <v-layout row align-center fill-height>
    <v-flex xs12 sm6 offset-sm3>
      <v-card>
        <v-list two-line>
          <template v-for="(user, index) in users">
            <v-divider v-if="user.divider" :key="index" :inset="user.inset"></v-divider>

            <v-list-tile v-else :key="index" avatar @click="userDetail(user)">
              <v-list-tile-avatar>{{user.id}}</v-list-tile-avatar>

              <v-list-tile-content>
                <v-list-tile-title v-html="user.firstName"></v-list-tile-title>
                <v-list-tile-sub-title v-html="user.lastName"></v-list-tile-sub-title>
              </v-list-tile-content>
              <v-list-tile-action>
                <v-icon>arrow_forward_ios</v-icon>
              </v-list-tile-action>
            </v-list-tile>
          </template>
        </v-list>
      </v-card>
    </v-flex>
  </v-layout>
</template>
<script>
export default {
  data() {
    return {
      users: [
        {
          id: 1,
          firstName: "Thavorn",
          lastName: "Khanthavong"
        },

        { divider: true, inset: true },
        {
          id: 2,
          firstName: "Charuda",
          lastName: "Luanglath"
        },
        { divider: true, inset: true },
        {
          id: 3,
          firstName: "Shawn",
          lastName: "Duan"
        }
      ]
    };
  },
  methods: {
    userDetail: function(user) {
      this.$router.push(
        "/user/" + user.firstName + "-" + user.lastName + "-" + user.id
      );
    }
  }
};
</script>