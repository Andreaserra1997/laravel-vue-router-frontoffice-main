<script></script>

<template>
  <div class="container mx-auto">
    <div class="about-section px-5 mb-5">
      <h1 class="mb-3">About Us</h1>
      <p>
        Creare Cocktail è un'arte, si sa, e come ogni pittore possiede il suo
        stile, ogni Mixologist può eseguire una ricetta cocktail secondo delle
        varianti suggerite dal suo sapere, oltre che dal mestiere di barman. Si
        scelgono dosi, strumenti e attrezzature bar adeguate, si studiano le
        diluizioni e le interazioni tra distillati e bevande. Non creiamo semplici
        cocktail ma esperienze sensoriali che coinvolgono tutti i nostri sensi,
        dalla vista, attraverso l'estetica e il dettaglio dei nostri cocktail, al
        gusto particolare, ricercato, raffinato che vi farà scoprire nuove
        frontiere del sapore. Ubriacatevi di Arte!
      </p>
    </div>

    <h3 class="text-white text-center">Our Team</h3>
    <div class="row">
      <div class="column">
        <div class="card">
          <img src="https://picsum.photos/200" alt="Gabriella Valentina">
          <div class="container">
            <h2>Gabriella Valentina</h2>
            <p class="title">CEO & Founder</p>
            <p>Some text that describes me lorem ipsum ipsum lorem.</p>
            <p>jane@example.com</p>
            <p><button class="button">Contact</button></p>
          </div>
        </div>
      </div>

      <div class="column">
        <div class="card">
          <img src="https://picsum.photos/200" alt="Gianluca Ligori">
          <div class="container">
            <h2>Gianluca Ligori</h2>
            <p class="title">Art Director</p>
            <p>Some text that describes me lorem ipsum ipsum lorem.</p>
            <p>mike@example.com</p>
            <p><button class="button">Contact</button></p>
          </div>
        </div>
      </div>

      <div class="column">
        <div class="card">
          <img src="https://picsum.photos/200" alt="Andrea Serra">
          <div class="container">
            <h2>Andrea Serra</h2>
            <p class="title">Art Director</p>
            <p>Some text that describes me lorem ipsum ipsum lorem.</p>
            <p>mike@example.com</p>
            <p><button class="button">Contact</button></p>
          </div>
        </div>
      </div>

      <div class="column">
        <div class="card">
          <img src="https://picsum.photos/200" alt="Matteo Mancuso">
          <div class="container">
            <h2>Matteo Mancuso</h2>
            <p class="title">Art Director</p>
            <p>Some text that describes me lorem ipsum ipsum lorem.</p>
            <p>mike@example.com</p>
            <p><button class="button">Contact</button></p>
          </div>
        </div>
      </div>

      <div class="column">
        <div class="card">
          <img src="https://picsum.photos/200" alt="Gabriele Barcellona">
          <div class="container">
            <h2>Gabriele Barcellona</h2>
            <p class="title">Designer</p>
            <p>Some text that describes me lorem ipsum ipsum lorem.</p>
            <p>john@example.com</p>
            <p><button class="button">Contact</button></p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
h2 {
  font-size: 1.3rem;
}

.column {
  width: 20%;
  padding: 0 8px;
}

.card {
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
  margin: 8px;
}

.about-section {
  text-align: center;
  color: white;
}

.container {
  padding: 0 16px;
}

.container::after,
.row::after {
  content: "";
  clear: both;
  display: table;
}

.title {
  color: grey;
}

.button {
  border: none;
  display: inline-block;
  padding: 8px;
  color: white;
  background-color: #000;
  text-align: center;
  cursor: pointer;
  width: 100%;
}

.button:hover {
  background-color: #555;
}

@media screen and (max-width: 650px) {
  .column {
    width: 100%;
    display: block;
  }
}
</style>
