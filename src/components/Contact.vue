<template>
  <footer id="contact">
    <hr class="line-separator" />
    <h1>Contact</h1>
    <div style="margin: 0px 24px;">
      <p class="desc">
        At <span style="color: #6d9eeb">Pho</span>
        {{ "" }}
        <span style="color: #dd7e6b">Than Brothers</span>, we strive for the
        best quality food and experience. We'd love your feedback.
      </p>
      <ul style="text-align: left; padding-left: 0px">
        <li>{{ email }}</li>
        <li>{{ address }}</li>
        <li>{{ phone }}</li>
      </ul>
    </div>
  </footer>
</template>

<script>
export default {
  data: function () {
    return {
      email: "chi@thanbrothers.com",
      address: "PO BOX 27529 Seattle, WA 98165",
      phone: "(206) 527-5973",
      emailValue: null,
      messageValue: null,
      errors: [],
    };
  }
};
</script>

<style lang="scss" scoped>
ul li {
  letter-spacing: 0px;
  color: #3d3d3d;
  font-family: "Courier New", Courier, monospace;
}

h1 {
  @include section-title-size;
  margin-bottom: 0px;
}
.submit-row {
  display: flex;
  justify-content: center;
}
#contact {
  bottom: 0;
  padding: 70px 0px;
  font-weight: 300;

  display: flex;
  flex-direction: column;
  align-items: center;
}
form {
  color: black;
  text-align: left;
}
textarea {
  margin: 0px;
  resize: none;
  height: 200px;
}
input,
textarea {
  width: 100%;
  border-width: 1px;
  padding: 7px 0px 7px 5px;
  border-style: solid;
  border-color: #ddd;
  margin-top: 10px;
  margin-bottom: 10px;
}
input,
textarea,
button {
  font-family: $default-font;
  font-size: 1em;
  color: black;
  font-weight: inherit;
}
.desc {
  color: black;
  width: 100%;
  max-width: 500px;
  text-align: left;
}
#send-button {
  border-style: solid;
  border-width: 1px;
  border-color: $red;
  background-color: white;
  color: $red;
  padding: 0px 40px;
  height: 40px;
  margin-bottom: 30px;
  transition: background-color 100ms, color 100ms;
  border-radius: 50px;

  &:hover {
    color: white;
    background-color: $red;
  }
}

p {
  color: rgb(136, 136, 136);
}
</style>
