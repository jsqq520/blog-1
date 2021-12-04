<template>
  <div id="gitalk-container"></div>
</template>

<script>
export default {
  name: "blog-comments",
  mounted() {
    const commentConfig = {
      // 是否开启
      enable: true,
      // clientID
      clientID: "5ee42da05cc337840383",
      // clientSecret
      clientSecret: "08bc031e767423189257214016cef919749ba8fd",
      // 评论项目名
      repo: "blog-comments",
      owner: "umiqq",
      admin: ["umiqq"],
      githubID: "umiqq",
      id: decodeURI(window.location.pathname),
      language: "zh-CN",
      distractionFreeMode: true,
    }
    const gitalk = new Gitalk(commentConfig)
    gitalk.render("gitalk-container")
  },
}
</script>
