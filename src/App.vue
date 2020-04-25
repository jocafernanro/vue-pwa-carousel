<template>
  <div id="app">
    <main>
      <div class="section">
        <h2>{{this.sections[0].headline}}</h2>
        <Carousel :cards="cards" />
      </div>
    </main>
  </div>
</template>

<script>
  import Carousel from "./components/Carousel";
  export default {
    name: "app",
    components: { Carousel },
    data() {
      return {
        sections: [
          { headline: "What can Service Workers do?" },
        ],
        cards: [
          {
            headline: "Make App available Offline",
            text: "All static files get pre-cached by using the Caching API.",
            imgName: "setting.svg"
          },
          {
            headline: "Use background sync to defer actions",
            text:
              "Data can be entered offline, it's sent when online again thanks to the Background Sync API.",
            imgName: "cloud.svg"
          },
          {
            headline: "Send Push Notifications",
            text:
              "The Notifications API lets us send push notifications to re-engage users.",
            imgName: "antenna.svg"
          }
        ]
      };
    }
  };
</script>

<style src="./assets/styles/App.css"/>
