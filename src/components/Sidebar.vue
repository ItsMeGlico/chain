<script setup></script>

<template>
  <div>
    <div class="IE6MIN">
      <div id="header" class="Header" role="banner">
        <div>
          <div class="Title">
            <a href="">LoginAdventure</a>
          </div>
          <div id="user">
            <!--로그인 여부-->
            <LoginView />
          </div>
        </div>
      </div>
    </div>
    <div class="Info">
      <footer class="Footer">
        <span>공지사항</span>
      </footer>
    </div>
    <div class="bar"></div>

    <main class="View">
      <div id="map" style="width: 100%; height: 100%"></div>
    </main>
  </div>
</template>

<style scoped></style>
