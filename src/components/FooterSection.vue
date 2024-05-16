<script setup>
const pages = { Books: "/", Documentry: "/", Careers: "/", Articles: "/" };
const follow = { Discord: "/", Twitter: "/", Instagram: "/", Medium: "/" };
const legals = { Privacy: "/", Contract: "/", Support: "/" };
</script>

<template>
  <section>
    <div>
      <div>
        <h2>Subscribe to our Newsletter</h2>
        <form>
          <input
            type="email"
            name="email"
            id="email"
            placeholder="Enter Your Email"
          />
          <button type="submit">Join the Newsletter</button>
        </form>
      </div>
      <div>
        <div>
          <h5>Pages</h5>
          <ul>
            <li v-for="(value, key, index) in pages" :key="index">
              <a :href="value">{{ key }}</a>
            </li>
          </ul>
        </div>
        <div>
          <h5>Follow</h5>
          <ul>
            <li v-for="(value, key, index) in follow" :key="index">
              <a :href="value">{{ key }}</a>
            </li>
          </ul>
        </div>
        <div>
          <h5>Legals</h5>
          <ul>
            <li v-for="(value, key, index) in legals" :key="index">
              <a :href="value">{{ key }}</a>
            </li>
          </ul>
        </div>
      </div>
    </div>
    <div>
      <p>
        &copy;
        <a href="https://twitter.com/StanleyAzi" target="_blank"
          >Stanley Azi (Frontend Dev)</a
        >
        &
        <a href="https://twitter.com/Austine_Ifenna" target="_blank"
          >Austine Ifenna (Web Designer)</a
        >
      </p>
      <a href="/">Terms and Condition</a>
    </div>
  </section>
</template>
