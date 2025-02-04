<script setup lang="ts">
import Todos from "./components/Todos.vue";
import Node from "./components/Node.vue";

import { Authenticator } from "@aws-amplify/ui-vue";
import "@aws-amplify/ui-vue/styles.css";
</script>

<template>
  <main>
    <authenticator>
      <template v-slot="{ signOut }">
        <Node />
        <button @click="signOut">Sign Out</button>
      </template>
    </authenticator>
  </main>
</template>
