<template>
  <div class="board">
    <Board />
  </div>
</template>

<script>
// @ is an alias to /src
import Board from '../components/Board.vue'

export default {
  name: 'Board',
  components: {
    Board
  }
}
</script>
