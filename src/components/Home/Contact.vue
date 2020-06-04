<template>
  <div class="contact">
    <div class="demo-request">
      <div class="contact__container">
        <h1>Request a demo</h1>
        <p>If you would like to know more about us, please fill in your email so that we can send you a product demo. Our consultants are also available for a life demonstration.</p>
        <form action>
          <input
            type="email"
            name="email"
            placeholder="Email"
            required="required"
            class="demail demo"
          />
          <input type="text" name="company" placeholder="Company" required class="dcompany demo" />
          <input type="submit" class="btn1" value="Submit" />
        </form>
      </div>
    </div>
    <div class="contact__container">
      <div class="contact-us">
        <h1>We’d love to hear from you</h1>
        <form id="f1">
          <table style="width:100%">
            <tr>
              <th>
                <input
                  type="text"
                  name="firstname"
                  placeholder="First Name"
                  v-model="user.name"
                  required
                  class="fname"
                />
              </th>
              <th>
                <input
                  type="text"
                  name="lastname"
                  placeholder="Last Name"
                  v-model="user.name"
                  required
                  class="lname"
                />
              </th>
              <th>
                <input
                  type="text"
                  name="phone"
                  id="phone"
                  placeholder="Phone"
                  required
                  class="phone"
                />
              </th>
              <th>
                <input
                  type="email"
                  name="email"
                  placeholder="Email"
                  required="required"
                  v-model="user.email"
                  class="email"
                />
              </th>
            </tr>
            <tr>
              <th colspan="4">
                <textarea placeholder="Type your message here ..." cols="20" class="message"></textarea>
              </th>
            </tr>
          </table>

          <input type="submit" class="btn" value="Submit" />
        </form>
        <br />

        <form id="f2">
          <table style="width:100%">
            <tr>
              <th>
                <input
                  type="text"
                  name="firstname"
                  placeholder="First Name"
                  v-model="user.name"
                  required
                  class="fname"
                />
              </th>
            </tr>
            <tr>
              <th>
                <input
                  type="text"
                  name="lastname"
                  placeholder="Last Name"
                  v-model="user.name"
                  required
                  class="lname"
                />
              </th>
            </tr>
            <tr>
              <th>
                <input type="text" name="phone" placeholder="Phone" required class="phone" />
              </th>
            </tr>
            <tr>
              <th>
                <input
                  type="email"
                  name="email"
                  placeholder="Email"
                  required="required"
                  v-model="user.email"
                  class="email"
                />
              </th>
            </tr>
            <tr>
              <th>
                <textarea placeholder="Type your message here ..." cols="20" class="message"></textarea>
              </th>
            </tr>
          </table>
          <input type="submit" class="btn" value="Submit" />
        </form>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      user: {
        name: "",
        email: ""
      }
    };
  }
};
</script>

<style lang="scss">
.contact {
  margin: 0;
  padding-bottom: 5rem;
  &__container {
    width: 70%;
    margin: 0 auto;
  }
}
.demo-request {
  background: #01c9dc;
  color: #fff;
  padding: 2rem 0 8rem 0;
  text-align: left;
  p {
    font-size: 2rem;
  }
}
h1 {
  padding: 4.2rem 0 3rem 0;
  font-size: 8rem;
  font-weight: 400;
}
.demo {
  border: 2px solid #fff;
  background: none;
  width: 35rem;
  display: block;
  margin: 3rem 0 3rem 0;
}

.btn1 {
  background: #fff;
  color: #01c9dc;
  width: 35rem;
  float: left;
  position: relative;
  cursor: pointer;
  &:hover {
    background: rgb(231, 229, 123);
  }
}
.contact-us {
  color: #01c9dc;
}
#f2 {
  display: none;
}
table {
  border-collapse: collapse;
}

th {
  border: 2px solid #01c9dc;
  margin: 0;
  &:hover {
    border-color: rgb(17, 183, 224);
  }
}
input {
  height: 7vh;
}
textarea {
  height: 15vh;
}
input,
textarea {
  padding: 2.5rem;
  font-size: 2rem;
  border: none;
  width: 100%;
  &:focus {
    outline: none;
  }
}
input[type="submit"] {
  padding: 1rem;
}
.btn {
  background: #01c9dc;
  color: #fff;
  cursor: pointer;
  margin-top: 3rem;
  &:hover {
    background: rgb(17, 183, 224);
  }
}
.fname::-webkit-input-placeholder,
.lname::-webkit-input-placeholder,
.phone::-webkit-input-placeholder,
.email::-webkit-input-placeholder,
.message::-webkit-input-placeholder {
  color: #01c9dc;
}
.demail::-webkit-input-placeholder,
.dcompany::-webkit-input-placeholder {
  color: #fff;
}
.message {
  resize: none;
}

@media only screen and (max-width: 992px) {
  #f1 {
    display: none;
  }
  #f2 {
    display: block;
  }
  table {
    border-collapse: separate;
    border-spacing: 1rem;
  }
  h1 {
    padding: 1rem 0 3rem 0;
    font-size: 5rem;
    font-weight: 400;
    text-align: left;
  }
  .demo-request {
    padding: 3rem 0 7rem 0;
    margin-bottom: 1;
  }
}
</style>
