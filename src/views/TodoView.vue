<template>
  <div class="todo">
    <v-list
      class="pt-0"
      flat
    >
    <div
      v-for="task in tasks"
      :key="task.id"
      >
        <v-list-item>
          <template v-slot:default="{ active, }">
            <v-list-item-action>
              <v-checkbox
                :input-value="active"
                color="primary"
              ></v-checkbox>
            </v-list-item-action>

            <v-list-item-content>
              <v-list-item-title>{{ task.title }}</v-list-item-title>
            </v-list-item-content>
          </template>
        </v-list-item>
      <v-divider></v-divider>
    </div>
    </v-list>
  </div>
</template>

<script>
import { upperFirst } from 'vuetify/lib/util/helpers'


  export default {
    name: 'Home',
    data() {
      return {
        tasks: [
          {
            id: 1,
            title: 'Wake upper'
          },
          {
            id: 2,
            title: 'Do push up'
          },
          {
            id: 3,
            title: 'Eat breakfast'
          }
        ]
      }
    }
  }
</script>
