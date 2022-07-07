<template>
  <div class="header-wrapper">
    <div class="container">
      <LayoutLogo></LayoutLogo>

      <div class="menu-wrapper">
        <ul class="d-flex">
          <li v-for="(item, index) in menuList" :key="index" class="mr-3">
            {{ item.text }}
            <div class="menu-wrapper__child">
              <p
                v-for="(child, jdex) in item.children"
                :key="jdex + child.text"
                >{{ child.text }}</p
              >
            </div>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
import LayoutLogo from "@/components/Layout/Logo.vue";

export default {
  name: "LayoutHeader",

  components: {
    LayoutLogo,
  },

  data() {
    return {
      abc: "vinml",
      menuList: [
        {
          text: "Home",
          url: "/",
          children: [
            { text: "Child", url: "/childadwad" },
            { text: "Child", url: "/childadwad" },
            { text: "Child", url: "/childadwad" },
          ],
        },
        { text: "Movies", url: "/", children: [] },
        { text: "Celebrities", url: "/", children: [] },
        { text: "News", url: "/", children: [] },
        { text: "My account", url: "/my-account", children: [] },
        { text: "Login", url: "/login", children: [] },
      ],
    };
  },
};
</script>
