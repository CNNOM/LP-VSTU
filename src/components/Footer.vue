<template>
  <footer class="footer">
    <div class="container">
      <div class="footer-content">
        <div class="footer-left">
          <span>Работа выполнена: Зенков Алексей Ильич</span>
        </div>
        <div class="footer-center">
          <img src="../assets/img/VSTU-logo-white.png" alt="Логотип" class="logo">
        </div>
        <div class="footer-right">
          <a href="https://github.com/CNNOM/CNNOM-IP_Dxracer" target="_blank" rel="noopener noreferrer"
             class="github-link">
            <img src="@/assets/img/git.png" alt="GitHub" class="github-logo">
            <span class="github-text">  GitHub</span>
          </a>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.footer {
  background-color: #333;
  color: #fff;
  padding: 10px 0;

  bottom: 0;
  width: 100%;
}

.footer-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.footer-left,
.footer-right {
  flex: 1;
  text-align: center;
  width: 33%;

}

a {
  color: white;
  text-decoration: none;

}

.footer-center {
  flex: 1;
  text-align: center;
  width: 33%;

}

.logo {
  max-width: 100px;
  height: auto;
}

.github-logo {
  max-width: 30px;
  height: auto;
  vertical-align: middle;
  border-radius: 50%;
  background-color: white;
}

.github-text {
  vertical-align: middle;
  margin-left: 5px;
}

.github-link {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100%;
}
</style>