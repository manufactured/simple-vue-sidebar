<template>
  <div class="sidebar">
    <div class="title">
      Yum Knowledge
    </div>
    <div class="menu-items">
      <router-link
        to="/"
        active-class="active"
        tag="button"
        exact
        class="side-btn"
      >
        <div class="link-container">
          Overview
        </div>
      </router-link>
      <router-link
        to="/messages"
        active-class="active"
        tag="button"
        exact
        class="side-btn"
      >
        <div class="link-container">
          Messages
        </div>
      </router-link>
      <router-link
        to="/profile"
        active-class="active"
        tag="button"
        exact
        class="side-btn"
      >
        <div class="link-container">
          Profile
        </div>
      </router-link>
      <router-link
        to="/settings"
        active-class="active"
        tag="button"
        exact
        class="side-btn"
      >
        <div class="link-container">
          Settings
        </div>
      </router-link>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.title {
  color: rgb(27, 27, 27);
  font-size: 16px;
  margin-top: 10px;
  padding: 10px;
  text-align: left;
  letter-spacing: -1px;
  text-transform: uppercase;
  font-weight: 800;
}

.menu-items {
  display: flex;
  flex-direction: column;
  margin-top: 40px;
  margin-left: 6px;
}

.menu-items > * {
  margin-top: 60px;
}

.side-btn {
  border: none;
  padding: 16px 0px;
  cursor: pointer;
  font-size: 16px;
  font-weight: 500;
  color: rgb(27, 27, 27);
  background-color: transparent;
}

.side-btn:focus {
  outline: none;
}

.side-btn.active {
  position: relative;
  background-color: rgb(27, 27, 27);
  color: rgb(14, 180, 103);
  font-weight: 600;
  margin-left: 10px;
  border-radius: 30px 0 0 30px;
}

.side-btn.active::before {
  top: -30px;
}

.side-btn.active::after {
  bottom: -30px;
}

.side-btn.active::before,
.side-btn.active::after {
  position: absolute;
  content: "";
  right: 0;
  height: 30px;
  width: 30px;
  background-color: rgb(27, 27, 27);
}

.side-btn.active .link-container::before {
  top: -60px;
}

.side-btn.active .link-container::after {
  bottom: -60px;
  z-index: 99;
}

.side-btn.active .link-container::before,
.side-btn.active .link-container::after {
  position: absolute;
  content: "";
  right: 0px;
  height: 60px;
  width: 60px;
  border-radius: 50%;
  background-color: rgb(14, 180, 103);
}
</style>
