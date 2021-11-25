<template>
  <section class="contact">
    <h2>Get In Touch With Us</h2>
    <form action="https://formspree.io/f/xayakjqr" method="POST" id="contact">
      <label for="name">Your Name</label>
      <input type="text" id="name" name="name" placeholder="Your Name" required>
      <label for="email">Your E-mail</label>
      <input type="email" id="email" name="email" placeholder="Your E-mail" required>
      <label for="subject">Subject</label>
      <textarea id="subject" name="subject" placeholder="Write Subject Here" required></textarea>
      <input type="submit" value="Submit">
    </form>
    <!-- MAP -->
    <iframe class="map" loading="lazy" allowfullscreen
      src="https://www.google.com/maps/embed/v1/place?key=AIzaSyBi_DA6iO6J5fdE7S0sSYR15o7AsWUm170&q=Calgary+AB">
    </iframe>
  </section>
</template>