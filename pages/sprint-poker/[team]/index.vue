<script setup>
import { onMounted } from 'vue'
import PokerTable from '~/components/SprintPoker/PokerTable'

let socket = null
const route = useRoute()
const ctx = useNuxtApp()
const teamName = route.params.team

const newMember = () => {
  socket.emit('newUserJoined', {
    hello: 'world',
  }, (resp) => {
    // TODO add logic
  })
}

onMounted(() => {
  socket = ctx.$nuxtSocket({
    name: 'main',
    channel: '/index',
    withCredentials: false,
  })
  /* Listen for events: */
  socket
    .on('newUserJoined', (msg, cb) => {
      // TODO add logic
    })
  newMember()
})
</script>

<template>
  <div class="flex justify-center items-center">
    <PokerTable />
  </div>
</template>
