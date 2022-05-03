<template>
  <main id="main">
    <div id="header">
      <Header />
    </div>
    <div id="banner">
      <Banner />
    </div>
    <div id="content">
      <Content />
    </div>
    <div class="aside">
      <Asided />
    </div>
    <div class="footer">
      <Footer />
    </div>
  </main>
</template>

<script>
import Header from '@/components/HeaderHome.vue';
import Banner from '@/components/BannerHome.vue';
import Content from '@/components/ContentHome.vue';
import Asided from '@/components/AssideHome.vue';
import Footer from '@/components/FooterHome.vue';

export default {
  name: 'HomeView',
  components: {
    Header,
    Banner,
    Content,
    Asided,
    Footer
  }
}
</script>
