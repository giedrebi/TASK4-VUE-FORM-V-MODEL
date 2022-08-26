<script>
export default {
  data() {
    return {
      fname: "",
      lname: "",
      pickedAge: '',
      selectedGender: '',
      checkedColor: [],
      message: ''
    };
  },
};
</script>

<template>
  <div>
    <form>
      <input v-model="fname" placeholder="Enter name" /><br />
      <input v-model="lname" placeholder="Enter surname" /><br />

      <p>Select your age group:</p>

      <input type="radio" id="one" value="18-25" v-model="pickedAge" />
      <label for="one"> 18-25</label><br>

      <input type="radio" id="two" value="older than 25" v-model="pickedAge" />
      <label for="two"> Older than 25</label>

      <p>Select your gender:</p>

      <select v-model="selectedGender">
        <option disabled value="">please select one</option>
        <option>male</option>
        <option>female</option>
        <option>other</option>
      </select>

      <p>Select colors you like (can be more than one):</p>

      <input type="checkbox" id="white" value="white" v-model="checkedColor" />
      <label for="white"> white </label>

      <input type="checkbox" id="black" value="black" v-model="checkedColor" />
      <label for="black"> black </label>

      <input type="checkbox" id="red" value="red" v-model="checkedColor" />
      <label for="red"> red </label>

      <input type="checkbox" id="yellow" value="yellow" v-model="checkedColor" />
      <label for="yellow"> yellow </label>

      <input type="checkbox" id="blue" value="blue" v-model="checkedColor" />
      <label for="blue"> blue </label>

      <input type="checkbox" id="green" value="green" v-model="checkedColor" />
      <label for="green"> green </label>

      <input type="checkbox" id="purple" value="purple" v-model="checkedColor" />
      <label for="purple"> purple </label>

      <input type="checkbox" id="none" value="none of these" v-model="checkedColor" />
      <label for="none"> none of these </label>

      <p>Add your comment:</p>

      <textarea v-model="message"></textarea>
    </form>

    <div class="answers">
      <p>Full name: {{ fname }} {{ lname }}</p>
      <p>Age group: {{ pickedAge }}</p>
      <p>Gender: {{ selectedGender }}</p>
      <p>Color/colors: {{ checkedColor }}</p>
      <p style="white-space: pre-line;">Your comment: {{ message }}</p>
    </div>

  </div>
</template>

<style scoped>
.answers,
form {
  border: 2px solid;
  border-radius: 10px;
  padding: 10px;
  margin-bottom: 10px;
  width: 550px;
}
textarea {
  height: 60px;
  width: 300px;
}

p {
  margin-top: 10px;
  margin-bottom: 10px;
}
</style>
