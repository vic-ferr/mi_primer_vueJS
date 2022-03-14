<template>
  <div id="app">
    <div class="container">
      <div class="row">
        <div class="col-12">
          <h1 class="display-1 mb-5">Proyecto de Vue!</h1>
        </div>
      </div>

      <div class="row">
        <div class="col-12">
          <table class="table">
            <thead>
              <tr>
                <th scope="col">#</th>
                <th scope="col">Nombre</th>
                <th scope="col">Apellido</th>
                <th scope="col">RUN</th>
                <th scope="col">Fecha de Nacimiento</th>
                <th scope="col">Edad</th>
              </tr>
            </thead>
            <tbody>
              <tr v-for="(persona, i) in personas" :key="i">
                <td>{{ i + 1 }}</td>
                <td>{{ persona.nombre }}</td>
                <td>{{ persona.apellido }}</td>
                <td>{{ persona.run }}</td>
                <td>{{ persona.fecha_nacimiento }}</td>
                <td>{{ persona.edad }}</td>
              </tr>
            </tbody>
          </table>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",

  data() {
    return {
      personas: [
        {
          nombre: "alberto",
          apellido: "garcia",
          run: "123",
          fecha_nacimiento: "20-10-72",
          edad: "50",
        },
        {
          nombre: "carlos",
          apellido: "rodriguez",
          run: "567",
          fecha_nacimiento: "20-10-82",
          edad: "40",
        },
        {
          nombre: "catalina",
          apellido: "perez",
          run: "891",
          fecha_nacimiento: "20-10-92",
          edad: "30",
        },
      ],
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
