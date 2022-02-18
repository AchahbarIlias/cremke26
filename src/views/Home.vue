<template>
<div>

  <!-- hero -->
  <section class="hero w-full bg-cones flex flex-col items-center justify-center mt-40 bg-background bg-blend-soft-light">
    <div class="grid grid-cols-1 gap-8 text-white">
      <h1 class="text-bold lg:text-9xl sm:text-8xl text-5xl">Cremke 26</h1>
      <div class="flex md:flex-row flex-col justify-between gap-8 mt-20 w-full">
        <button class="bg-green-400 p-4 rounded-sm w-full font-bold text-xl">Menu</button>
        <button class="bg-green-400 p-4 rounded-sm w-full font-bold text-xl">Openingsuren</button>
      </div>
    </div>
  </section>
  <!-- end hero -->

  <!-- menu -->
  <section class="container mx-auto px-8 md:px-14 lg:px-24 w-full mt-24">
    <div class="flex flex-col text-white border border-gray-400">
      <h2 class="bg-background py-8 text-4xl">Menu</h2>
      <div class="flex py-4 justify-around text-black bg-background text-white text-xl">
        <h3>Smaak</h3>
        <h3>Prijs</h3>
      </div>
      <div class="grid grid-cols-2 text-black border-b border-green-400 p-2.5 my-2" v-for="smaak in smaken" :key="smaak.id">
        <p>{{smaak.name}}</p>
        <p>{{smaak.price}}</p>
      </div>
    </div>
  </section>
  <!-- end menu -->

  <!-- locatie -->
  <section class="container mx-auto px-8 md:px-14 lg:px-24 w-full mt-24">
    <div class="grid xl:grid-cols-2 grid-cols-1 gap-8">
      <div class="">
        <h2 class="bg-background py-8 text-4xl text-white">Locatie</h2>
                <article class="flex justify-center items-center p-8 text-black">
          Kopstraat 1, Tienen (3300)
        </article>
          <iframe class="w-full" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2520.471651804747!2d4.974966115906223!3d50.82242706837278!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x47c16c9e0f4b88ef%3A0x13b6cc0ca6a6ccf0!2sKopstraat%201%2C%203300%20Tienen!5e0!3m2!1sen!2sbe!4v1645210065956!5m2!1sen!2sbe" width="800" height="450" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
      </div>

      <div class="flex flex-col">
        <h2 class="bg-background py-8 text-4xl text-white">Openingsuren</h2>
          <ul class="flex flex-col gap-4 mt-20">
            <li>Maandag: 9:00u - 17:00u</li>
            <li>Dinsdag: 9:00u - 17:00u</li>
            <li>Woensdag: 9:00u - 17:00u</li>
            <li>Donderdag: 9:00u - 17:00u</li>
            <li>Vrijdag: 9:00u - 17:00u</li>
            <li>Zaterdag: 9:00u - 17:00u</li>
            <li>Zondag: gesloten</li>
        </ul>
      </div>
    </div>
  </section>
  <!-- end locatie -->


</div>
</template>

<script>
export default {
  name: 'Hero',
  data() {
    return {
      smaken: [{"name": "vanille", "price": "2.50"}, {"name": "chocolade", "price": "2.50"}, {"name": "mokka", "price": "2.50"}, {"name": "citroen", "price": "2.50"}, {"name": "meloen", "price": "2.50"}, {"name": "rode vruchten", "price": "2.50"}]
    };
  },
}
</script>

<style>
.hero {
  height: 40rem;
}
</style>