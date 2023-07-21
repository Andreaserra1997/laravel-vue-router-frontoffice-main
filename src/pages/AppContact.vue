<script>
export default {};
</script>
<template>
  <h2>Contact us</h2>

  <form>
    <div class="mb-3" novalidate>
      <label for="name" class="form-label">Name</label>
      <input
        type="text"
        class="form-control"
        id="name"
        aria-describedby="emailHelp"
      />
    </div>

    <div class="mb-3">
      <label for="email" class="form-label">Email address</label>
      <input
        type="email"
        class="form-control"
        id="email"
        aria-describedby="emailHelp"
      />
    </div>

    <div class="mb-3">
      <label for="exampleFormControlTextarea1" class="form-label"
        >Message</label
      >
      <textarea
        class="form-control"
        id="exampleFormControlTextarea1"
        rows="3"
      ></textarea>
    </div>

    <div class="mb-3 form-check">
      <input type="checkbox" class="form-check-input" id="exampleCheck1" />
      <label class="form-check-label" for="exampleCheck1"
        >subscribe to the NewsLetters</label
      >
    </div>

    <button type="submit" class="btn btn-primary">Submit</button>
  </form>
</template>

<style lang="scss" scoped></style>
