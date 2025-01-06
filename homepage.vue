<template>
  <div id="app" class="layout">
    <!-- Sidebar -->
    <aside class="sidebar">
      <div class="logo">LIEBHERR</div>
      <nav class="menu">
        <button class="menu-item active">
          <i class="icon-home"></i>
          <span>Home</span>
        </button>
        <button class="menu-item">
          <i class="icon-map"></i>
          <span>Map</span>
        </button>
        <button class="menu-item">
          <i class="icon-settings"></i>
          <span>Settings</span>
        </button>
        <button class="menu-item">
          <i class="icon-user"></i>
          <span>Profile</span>
        </button>
      </nav>
      <div class="footer">
        <button class="expand">
          <i class="icon-expand"></i>
        </button>
        <div class="user-icon">JD</div>
      </div>
    </aside>

    <!-- Main Content -->
    <main class="main-content">
      <header class="topbar">
        <div class="topbar-content">
          <div class="language">
            EN
            <i class="icon-globe"></i>
          </div>
          <i class="icon-search"></i>
          <i class="icon-user-circle"></i>
        </div>
      </header>
      <section class="content">
        <h1>Home page</h1>
      </section>
    </main>
  </div>
</template>

<script lang="ts">
export default {
  name: 'App',
};
</script>

<style scoped>
/* Layout */
.layout {
  display: flex;
  height: 100vh;
  background-color: #f4f4f4;
}

/* Sidebar */
.sidebar {
  width: 80px;
  background-color: #fff;
  display: flex;
  flex-direction: column;
  align-items: center;
  border-right: 1px solid #e6e6e6;
}

.sidebar .logo {
  font-weight: bold;
  font-size: 16px;
  margin: 20px 0;
  text-align: left; /* จัดข้อความชิดซ้าย */
  width: 100%; /* ยืดเต็มพื้นที่ sidebar */
  padding-left: 10px; /* เพิ่มระยะห่างจากขอบซ้าย */
}

.menu {
  flex-grow: 1;
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.menu-item {
  width: 100%;
  background: none;
  border: none;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 10px 0;
  color: #555;
  cursor: pointer;
}

.menu-item.active,
.menu-item:hover {
  background-color: #ffd700;
  color: #000;
}

.menu-item i {
  font-size: 20px;
}

.menu-item span {
  font-size: 12px;
}

/* Footer */
.footer {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 10px;
  margin-bottom: 20px;
}

.expand {
  background: none;
  border: none;
  cursor: pointer;
}

.user-icon {
  width: 40px;
  height: 40px;
  background-color: #ccc;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: bold;
}  w3 

/* Main Content */
.main-content {
  flex: 1;
  display: flex;
  flex-direction: column;
}

.topbar {
  display: flex;
  justify-content: flex-end;
  align-items: center;
  padding: 10px 20px;
  background-color: #fff;
  border-bottom: 1px solid #e6e6e6;
}

.topbar-content {
  display: flex;
  align-items: center;
  gap: 20px;
}

.language {
  display: flex;
  align-items: center;
  gap: 5px;
  cursor: pointer;
}

.content {
  padding: 20px;
}

.content h1 {
  font-size: 24px;
  font-weight: bold;
}
</style>
