<template>
  <footer class="py-5">
    <div class="container">
      <div class="d-flex flex-column justify-content-around flex-md-row text-center mt-5 text-white">
        <a class="mb-3" href="#"><img src="/images/logo.svg" alt="" /></a>

        <div class="mb-3" v-for="info in infos" :key="info.id">
          <p>{{info.title}}</p>

          <ul>
            <li>{{info.item1}}</li>
            <li>{{info.item2}}</li>
            <li>{{info.item3}}</li>
            <li>{{info.item4}}</li>
            <li>{{info.item5}}</li>
          </ul>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
    data() {
        return {
            infos: [
                {title: "Product", item1: "Overview", item2: "Pricing", item3: "Marketplace", item4: "Features", item5: "Integrations"},

                {title: "Company", item1: "About", item2: "Team", item3: "Blog", item4: "Careers"},

                {title: "Connect", item1: "Contact", item2: "Newsletter", item3: "Linkedin"},
            ]
        }
    }
};
</script>

<style scoped>
footer {
  background-color: var(--clr-very-dark-gray-blue);
  border-top-right-radius: 100px;
}

li {
    color: var(--clr-very-dark-grayish-blue) !important;
}
</style>