<template>
  <div class="signup">
    <h1 class="text-center mb-5">Signup</h1>
   
    <div class="container">
      <div class="row">
        <div class="col"></div>
        <div class="col">
          <form>
            <div class="form-group">
              <label for="emailField">Email address</label>
              <input type="email" class="form-control" id="emailField" aria-describedby="emailHelp" placeholder="Enter email">
              <small id="emailHelp" class="form-text text-muted">We'll never share your email with anyone else.</small>
            </div>
            <div class="form-group">
              <label for="passwordField">Password</label>
              <input type="password" class="form-control" id="passwordField" placeholder="Password">
            </div>
            <div class="form-group">
              <label for="confirmPasswordField">Confirm Password</label>
              <input type="password" class="form-control" id="confirmPasswordField" placeholder="Confirm Password">
            </div>
            <button type="submit" class="btn btn-primary mt-5">Submit</button>
          </form>
        </div>
        <div class="col"></div>
      </div>
     </div>  
  </div>
</template>
