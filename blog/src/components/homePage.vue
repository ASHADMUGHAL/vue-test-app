<!-- <template>
<div>
    <h2>Task 6: Password Confirmation</h2>
    <input type="password" v-model="password" placeholder="Enter Password" />
    <input type="password" v-model="confirmPassword" placeholder="Confirm Password" />
    <p :style="{ color: passwordMatch ? 'green' : 'red' }">
        {{ passwordMatch ? "Passwords match" : "Passwords do not match" }}
    </p>
</div>
</template>

<script>
export default {
    name: "PasswordConfirmation",
    data() {
        return {
            password: "",
            confirmPassword: "",
        };
    },
    computed: {
        passwordMatch() {
            return this.password === this.confirmPassword;
        },
    },
};
</script>
<script>
    -- >
    <
    !-- < template >
        <
        div >
        <
        h2 > Task 7: Dynamic Heading < /h2> <
    input
    v - model = "headingText"
    placeholder = "Type heading text"
    style = "
    height: 10 px;
    width: 120 px;
    padding: 10 px;
    border: 1 px solid# ccc;
    border - radius: 4 px;
    background - color: beige;
    " / >
    <
    h1 > {
            {
                headingText
            }
        } < /h1> < /
        div > <
        /template>

    export default {
        name: "DynamicHeading",
        data() {
            return {
                headingText: "",
            };
        },
    };
</script><script>
 -- >

 <
 !-- < template >
     <
     div >
     <
     h2 > Task 8: Show / Hide Password < /h2> <
     input: type = "showPassword ? 'text' : 'password'"
 v - model = "passwordToggle" / >
     <
     label > < input type = "checkbox"
 v - model = "showPassword" / > Show Password < /label> <
     /div> <
     /template>

 export default {
     data() {
         return {
             passwordToggle: "",
             showPassword: false,
         };
     },
 };
</script> -->
<!-- 
<template>
  <div>
    <h2>Task 8: Show/Hide Password</h2>
    <input :type="showPassword ? 'text' : 'password'"
      v-model="passwordToggle"
      placeholder="Enter your password"
    />
    <label>
      <input type="checkbox" v-model="showPassword" />
      Show Password
    </label>
  </div>
</template>

<script>
export default {
  name: "ShowHidePassword",
  data() {
    return {
      passwordToggle: "",
      showPassword: false,
    };
  },
};
</script>

<style scoped>
.container {
  width: 400px;
  margin: 50px;
  padding: 20px;
  background: #f2f2f2;
  border-radius: 12px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  font-family: Arial, sans-serif;
}

h2 {
  text-align: center;
  margin-bottom: 20px;
  /* color: #333; */
}

.password-input {
  width: 100%;
  padding: 10px;
  border: 2px solid #ccc;
  border-radius: 8px;
  font-size: 16px;
  transition: border-color 0.3s;
  box-sizing: border-box;
}

.checkbox-label {
  display: flex;
  align-items: center;
  margin-top: 15px;
  font-size: 14px;
  color: #333;
}

.checkbox-label input {
  margin-right: 8px;
}
</style> -->

<!-- <template>
  <div>
    <h2>Task 9: Character Counter</h2>
    <textarea v-model="charText" placeholder="Type something..."></textarea>
    <p>Characters: {{ charText.length }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      charText: "",
    };
  },
};
</script> -->

<!-- <template>
  <input
    :value="modelValue"
    @input="$emit('update:modelValue', $event.target.value)"
    placeholder="Custom input"
  />
</template>

<script>
export default {
  props: {
    modelValue: String,
  },
};
</script> -->

<!-- <template>
  <div>
    <input v-model="username" placeholder="Type your name" />
    <p>Username: {{ username }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      username: "",
    };
  },
  watch: {
    username(newVal, oldVal) {
      `Username changed from ${oldVal} to ${newVal}`;
    },
  },
};
</script> -->

<!-- <template>
  <div>
    <input v-model="username" placeholder="Type your name" />
    <p>Username: {{ username }}</p>
    <p v-if="oldUsername">Previous Username: {{ oldUsername }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      username: "",
      oldUsername: "",
    };
  },
  watch: {
    username(newVal, oldVal) {
      this.oldUsername = oldVal; // Store previous username in data property
    },
  },
};
</script> -->

<!-- <template>
  <div>
    <input v-model="name" placeholder="Type your name" />
    <p>Your name is: {{ name }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: "",
    };
  },
  watch: {
    name(newValue, oldValue) {
      if (newValue.length > 6) {
        alert(`You changed your name from "${oldValue}" to "${newValue}"`);
      }
    },
  },
};
</script> -->

<!-- <template>
  <div class="price-calculator">
    <h2>Price Calculator</h2>
    <div class="input-group">
      <label for="quantity">Quantity:</label>
      <input
        id="quantity"
        v-model.number="quantity"
        type="number"
        min="0"
        placeholder="Enter quantity"
        class="quantity-input"
      />
    </div>
    <p class="total-price">
      Total Price: <span>${{ totalPrice.toFixed(2) }}</span>
    </p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      quantity: 0,
      totalPrice: 0,
      pricePerUnit: 50,
    };
  },
  watch: {
    quantity() {
      this.totalPrice = this.quantity * this.pricePerUnit;
    },
  },
};
</script>

<style scoped>
.price-calculator {
  max-width: 400px;
  margin: 2rem auto;
  padding: 2rem;
  border-radius: 8px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
  background-color: #ffffff;
  font-family: "Arial", sans-serif;
}

h2 {
  color: #2c3e50;
  margin-top: 0;
  margin-bottom: 1.5rem;
  text-align: center;
  font-weight: 600;
}

.input-group {
  margin-bottom: 1.5rem;
}

label {
  display: block;
  margin-bottom: 0.5rem;
  color: #5a6474;
  font-weight: 500;
}

.quantity-input {
  width: 100%;
  padding: 0.75rem;
  border: 2px solid #dcdfe6;
  border-radius: 4px;
  font-size: 1rem;
  transition: border-color 0.3s;
  box-sizing: border-box;
}

.quantity-input:focus {
  border-color: #409eff;
  outline: none;
}

.total-price {
  padding: 1rem;
  background-color: #f8f9fa;
  border-radius: 4px;
  font-size: 1.1rem;
  text-align: center;
  color: #2c3e50;
}

.total-price span {
  font-weight: bold;
  color: #409eff;
}
</style> -->
<!-- 
<template>
  <div>
    <button v-on:click="showMessage = !showMessage">Toggle Message</button>
    <p v-if="showMessage">Hello, Vue!</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showMessage: true,
    };
  },
};
</script> -->

<!-- <template>
  <div>
    <p v-if="value > 10">Value is greater than 10</p>
    <p v-else-if="value === 10">Value equals 10</p>
    <p v-else>Value is less than 10</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      value: 10,
    };
  },
};
</script> -->

<!-- <template>
  <div>
    <input v-model="inputValue" placeholder="Type something" />
    <p v-if="!inputValue">Input cannot be empty</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      inputValue: "",
    };
  },
};
</script> -->

<!-- <template>
  <div>
    <input v-model="items" />
    <ul>
      <li v-for="item in items" :key="item">{{ item }}</li>
    </ul>
    <p v-if="items.length === 0">No items in the list</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: ["ashad"],
    };
  },
};
</script> -->

<!-- <template>
  <p v-if="isLoggedIn">Welcome back!</p>
</template>
<script>
export default {
  data() {
    return {
      isLoggedIn: true,
    };
  },
};
</script> -->

<!-- 
<template>
  <p v-if="age < 18">You are underage</p>
  <p v-else>You are an adult</p>
</template>
<script>
export default {
  data() {
    return {
      age: 20,
    };
  },
};
</script> -->

<!-- <template>
  <p v-if="isLoading">Loading...</p>
</template>
<script>
export default {
  data() {
    return {
      isLoading: true,
    };
  },
};
</script> -->
<!-- 
<template>
  <p v-if="isError">Something went wrong!</p>
</template>
<script>
export default {
  data() {
    return {
      isError: true,
    };
  },
};
</script> -->

<!-- <template>
  <p v-if="status === 'sucess'">Operation successful</p>
  <p v-else-if="status === 'error'">Operation failed</p>
  <p v-else>status unknown</p>
</template>
<script>
export default {
  data() {
    return {
      status: "sucess",
    };
  },
};
</script> -->

<!-- <template>
  <div>
  
    <div v-if="!isLoggedIn">
      <p>Please login</p>
      <form>
        <label for="username">Username:</label>
        <input
          id="username"
          v-model="username"
          type="text"
          placeholder="Enter username"
        />

        <label for="password">Password:</label>
        <input
          id="password"
          v-model="password"
          type="password"
          placeholder="Enter password"
        />

        <button @click.prevent="login">Login</button>
      </form>
    </div>
  
    <div v-else>
      <p>Welcome back, {{ username }}!</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isLoggedIn: false,
      username: "",
      password: "",
    };
  },
  methods: {
    login() {
      if (this.username && this.password) {
        // Simulate login logic
        this.isLoggedIn = true;
      } else {
        alert("Please enter both username and password.");
      }
    },
  },
};
</script> -->

<!-- <template>
  <div v-if="!isLoggedIn">
    <p>Please log in</p>
    <input type="text" placeholder="Username" />
    <input type="password" placeholder="Password" />
    <button @click="login">Login</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isLoggedIn: false,
    };
  },
  methods: {
    login() {
      this.isLoggedIn = true;
    },
  },
};
</script> -->
<!-- 
<template>
  <p v-if="!isHide">a quick brown fox jumps over the lazy dog</p>
</template>
<script>
export default {
  data() {
    return {
      isHide: true,
    };
  },
};
</script> -->

<template>
  <div style="padding: 20px; max-width: 400px">
    <h2>🧮 Discount Calculator</h2>

    <input type="number" v-model="price" placeholder="Enter price" />
    <br /><br />
    <input type="number" v-model="quantity" placeholder="Enter quantity" />
    <br /><br />
    <input type="number" v-model="discount" placeholder="Enter discount %" />
    <br /><br />

    <p>🔹 Total (no discount): {{ totalWithoutDiscount }}</p>
    <p>🔻 Discount Amount: {{ discountAmount }}</p>
    <p>💰 Final Price: {{ finalTotal }}</p>
    <p>💡 Final (method): {{ getFinalTotal() }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      price: 0,
      quantity: 0,
      discount: 0,
    };
  },
  computed: {
    totalWithoutDiscount() {
      return this.price * this.quantity;
    },
    discountAmount() {
      return (this.totalWithoutDiscount * this.discount) / 100;
    },
    finalTotal() {
      return this.totalWithoutDiscount - this.discountAmount;
    },
  },
  methods: {
    getFinalTotal() {
      // Method version (not cached)
      const total = this.price * this.quantity;
      const discountValue = (total * this.discount) / 100;
      return total - discountValue;
    },
  },
};
</script>
