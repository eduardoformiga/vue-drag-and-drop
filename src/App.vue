<template>
  <div id="app">
    <main class="flexbox">
      <Board id="board-1">
        <Card
          id="card-1"
          draggable="true"
        >
          <p>Card One</p>
        </Card>
      </Board>

      <Board id="board-2">
        <Card
          id="card-2"
          draggable="true"
        >
          <p>Card Two</p>
        </Card>
      </Board>
    </main>
  </div>
</template>

<script>
import Board from './components/Board'
import Card from './components/Card'
export default {
  name: 'app',
  components: { Board, Card }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;

  --body-bg-color: #f3f3f3;
  --board-bg-color: #313131;
}

body {
  background-color: var(--body-bg-color);
}

.flexbox {
  display: flex;
  justify-content: space-between;

  width: 100%;
  max-width: 768px;
  height: 100vh;

  overflow: hidden;

  margin: 0 auto;
  padding: 15px;
}

.flexbox .board {
  display: flex;
  flex-direction: column;

  width: 100%;
  max-width: 300px;

  background-color: var(--board-bg-color);
  padding: 15px;
}

.flexbox .board .card {
  padding: 15px 25px;
  background-color: var(--body-bg-color);

  cursor: pointer;
  margin-bottom: 15px;
}
</style>
