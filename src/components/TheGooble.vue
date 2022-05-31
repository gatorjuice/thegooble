<template>
  <div>
    <h1>The Gooble</h1>
  </div>
  <div class="mdl-grid">
    <div class="mdl-cell mdl-cell--3-col"></div>
    <div class="mdl-cell mdl-cell--6-col">
      <form action="#" @submit.prevent="submitQuery">
        <div class="mdl-textfield mdl-js-textfield">
          <input
            class="mdl-textfield__input"
            type="text"
            id="query"
            v-model="query"
          />
          <label class="mdl-textfield__label" for="query">Search...</label>
        </div>
        <div>
          <button
            type="submit"
            @click="submitQuery"
            class="mdl-button mdl-js-button mdl-button--raised mdl-js-ripple-effect"
          >
            The Gooble it!
          </button>
        </div>
      </form>
    </div>
    <div class="mdl-cell mdl-cell--3-col"></div>
  </div>
  <div>
    <p>{{ results }}</p>
  </div>
</template>
<script>
export default {
  data() {
    return {
      results: "",
    };
  },
  mounted() {
    this.results = "";
  },
  methods: {
    submitQuery() {
      if (this.query.toLowerCase() != "earthworms") {
        this.results = "You spelled EARTHWORMS wrong";
      } else {
        this.results =
          "Earthworms are a type of worm that are subdermal if the planet was skin.";
      }
    },
  },
};
</script>
<style></style>
