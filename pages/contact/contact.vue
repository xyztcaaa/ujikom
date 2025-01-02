<template>
  <div class="container">
    <div class="back-button">
      <nuxt-link to="/" class="d-flex align-items-center">
        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-caret-left-fill" viewBox="0 0 16 16">
          <path d="m3.86 8.753 5.482 4.796c.646.566 1.658.106 1.658-.753V3.204a1 1 0 0 0-1.659-.753l-5.48 4.796a1 1 0 0 0 0 1.506z"/>
        </svg>
        <span class="ms-2">Kembali</span>
      </nuxt-link>
    </div>
    <div style="text-align:center">
      <h2>Contact Us</h2>
    </div>
    <div class="row">
      <div class="column">
        <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3957.2131636317426!2d108.25189907404213!3d-7.32993997208793!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x2e6f59eeb6bda36f%3A0xa9e724a275da6c2d!2sSMK%20Negeri%204%20Tasikmalaya!5e0!3m2!1sid!2sid!4v1734660682140!5m2!1sid!2sid" width="600" height="450"  loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
      </div>
      <div class="column">
        <form onsubmit="return false;">
          <label for="fname">First Name</label>
          <input type="text" id="fname" name="firstname" placeholder="Your first name..">
          
          <label for="email">Email Address</label>
          <input type="email" id="email" name="email" placeholder="Your email address..">
          
          <label for="subject">Subject</label>
          <textarea id="subject" name="subject" placeholder="Your message.." style="height:170px"></textarea>
          <button type="button" class="submit-btn">Submit</button> 
        </form>
      </div>
    </div>
  </div>
  
</template>
<script setup>
useHead({
  title: 'Contact Us - SMK Negeri 4 Tasikmalaya',
  meta: [
    {
      name: 'description',
      content: 'Contact Us - SMK Negeri 4 Tasikmalaya',
    },
  ],
});
</script>

<style scoped>
iframe {
    width: 90%;
    height: 350px
}

body {
  font-family: Arial, Helvetica, sans-serif;
  margin: 0;
  padding: 0;
  background-color: #f9f9f9;
}

* {
  box-sizing: border-box;
}

/* Back button styling */
.back-button {
  margin-bottom: 20px;
}

.back-button a {
  text-decoration: none;
  color: #04AA6D;
  font-size: 16px;
}

.back-button a:hover {
  color: #45a049;
}

input[type=text], input[type=email], select, textarea {
  width: 100%;
  padding: 12px;
  border: 1px solid #ccc;
  border-radius: 4px;
  margin-top: 6px;
  margin-bottom: 16px;
  resize: vertical;
  font-size: 14px;
}

.submit-btn {
  background-color: #04AA6D;
  color: white;
  padding: 12px 20px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  font-size: 16px;
  transition: background-color 0.3s ease;
}

.submit-btn:hover {
  background-color: #45a049;
}

.container {
  border-radius: 5px;
  padding: 20px;
  margin: 5rem auto;
  max-width: 900px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  margin-top: 9rem;
}

.column {
  float: left;
  width: 50%;
  margin-top: 6px;
  padding: 20px;
}

/* Clear floats after the columns */
.row:after {
  content: "";
  display: table;
  clear: both;
}

/* Responsive layout */
@media screen and (max-width: 600px) {
  .column {
    width: 100%;
    margin-top: 0;
    padding: 10px;
  }

  .submit-btn {
    width: 100%;
  }
}
</style>
