<template>
  <!--Yeah there's just no any sub components here cause I'm lazy.-->
  <el-container>
    <el-header>
      <h1>The Homepage of XCTRA —— XAUFE Computer Technology Research Association</h1>
    </el-header>
    <el-main>
      <img src="./assets/misbrands.png" alt="Misbrands Logo" style="max-width: 100%; max-height: 100%"/>
      <el-divider/>
      <el-card>
        <template #header>
          <h2>我们是谁</h2>
        </template>
        一群计算机技术爱好者，我们致力于计算机技术的研究与创新，我们的目标是为学校的计算机技术的发展贡献自己的力量。
        我们欢迎所有对计算机技术感兴趣的同学加入我们。
      </el-card>
      <el-divider/>
      <el-card>
        <template #header>
          <h2>我们平常干什么</h2>
        </template>
        聊天，吹水，做一切酷的事情！
      </el-card>
      <el-divider/>
      <el-card>
        <template #header>
          <h2>我们目前提供的服务</h2>
        </template>
        <a href="https://hole.xctra.cn">西财树洞</a> —— 匿名贴吧服务
        <br/><br/>
        <a href="https://blog.xctra.cn">XCTRA 博客</a> —— 技术交流与讨论
      </el-card>
      <el-divider/>
      <el-card>
        <template #header>
          <h2>我们的成员</h2>
        </template>
        <div style="display: flex; flex-direction: column">
          <member-card name="贺兰星辰"
                       email="shaokeyibb@126.com"
                       description="XCTRA 创始人，开发者"
                       github-id="shaokeyibb"></member-card>
          <member-card name="陈伯硕"
                       email="1085751402@qq.com"
                       description="西安财经大学 计算机科学与技术专业 2018 级毕业生；杭州电子科技大学计算机科学技术专业 2022 级研究生"
                       github-id="chenboshuo"></member-card>
          <member-card name="程驰"
                       email="3296661857@qq.com"
                       description="西安财经大学 计算机科学与技术专业 2019 级学生"
                       github-id="cc200723"></member-card>
          <member-card name="暗影月赎"
                       email="2014243824@qq.com"
                       description="鲁东大学 人工智能专业 2022 级学生"
                       :is-special="true"
                       github-id="AnyMoonS"></member-card>
          <member-card name="冰星"
                       email="625924077@qq.com"
                       description="某 211 高校 2019 级学生"
                       :is-special="true"
                       github-id="LovesAsuna"></member-card>
          <member-card name="蓝猫"
                       email="657399256@qq.com"
                       description="复旦大学 2020 级学生"
                       :is-special="true"
                       github-id="ABlueCat123"></member-card>
          <member-card name="one"
                       email="875899749@qq.com"
                       description="计算机图形学爱好者"
                       :is-special="true"
                       github-id="MorningOriens"></member-card>
          以及其他的小伙伴，也许，还将会有您...
        </div>
      </el-card>
      <el-divider/>
      <el-card>
        <template #header>
          <h2>如何加入我们</h2>
        </template>
        加入【西财计算机鱼塘】QQ群：<a href="https://jq.qq.com/?_wv=1027&k=MDOzxKsn" target="_blank">873123415</a>
      </el-card>
    </el-main>
    <el-footer>
      XCTRA Homepage ©2022 <a href="https://www.xctra.cn" target="_blank">XAUFE Computer Technology Research
      Association</a>, all
      rights reserved. 西财大计算机技术研究协会是一个由学生自发成立的技术研究组织，本组织与西安财经大学无从属关系。
      <a href="https://beian.miit.gov.cn/" target="_blank">陕ICP备2020016655号-2</a>
    </el-footer>
  </el-container>
</template>

<script setup>
import MemberCard from "./components/MemberCard.vue";
</script>

<style scoped>
</style>
