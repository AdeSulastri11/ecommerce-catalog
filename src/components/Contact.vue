<template>
  <div class="contact" id="contact">
    <form action="">
      <input type="text" name="" id="" placeholder="Username">
      <input type="password" name="" id="" placeholder="Password">
      <textarea name="" id="" cols="30" rows="10" placeholder="Message"></textarea>
      <div class="btn">
        <button type="submit">Submit</button>
      </div>
    </form>
    <iframe
      src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d127365.52505754633!2d122.45464150803211!3d-3.9848743333095142!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x2d98ecde0b6b7183%3A0x1397347f9e562fc7!2sKendari%2C%20Kota%20Kendari%2C%20Sulawesi%20Tenggara!5e0!3m2!1sid!2sid!4v1709546256997!5m2!1sid!2sid"
      width="100%" height="350" style="border:0;" allowfullscreen="" loading="lazy"
      referrerpolicy="no-referrer-when-downgrade"></iframe>
  </div>
</template>

<script>
export default {
  name: 'ContactUs',
}
</script>

<style>
.contact {
  display: grid;
  grid-template-columns: 2fr 2fr;
  padding: 50px 70px;
  gap: 30px;
}

form {
  display: flex;
  flex-direction: column;
  row-gap: 10px;
  padding: 0 15px;
}

form input {
  padding: 10px 10px;
  border-radius: 5px;
  border: 1px solid;
}
form textarea {
  padding: 10px;
}
.btn button {
  padding: 7px 18px;
  border-radius: 5px;
  border: none;
  background-color: #5b88dbd7;
  color: white;
  cursor: pointer;
}
.btn button:active{
  background-color: #5c90f1;
}
</style>