<template>
  <div class="home">
    <div class="container">
      <div class="accordeon">
        <FAQ v-for="(faq, i) in faqs" :faq="faq" :index="i" :key="i" :open="faq.open" @toggleOpen="toggleOpen" />
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import FAQ from "@/components/FAQ.vue"

export default {
  name: 'HomeView',
  components: {
    FAQ
  },
  data() {
    return {
      faqs: [
        {
          question: "To take into account on user level data",
          answer: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Tenetur odio veniam ut nobis, tempore ex laboriosam, quibusdam, accusamus odit debitis cumque commodi fugiat? Recusandae cupiditate, dolor necessitatibus non sequi repudiandae.",
          open: false
        },
        {
          question: "Our data",
          answer: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. ",
          open: false
        },
        {
          question: "Hands on analyzing",
          answer: "Tenetur odio veniam ut nobis, tempore ex laboriosam, quibusdam, accusamus odit debitis cumque commodi fugiat?",
          open: false
        },
        {
          question: "Initialization",
          answer: "Tenetur odio veniam ut nobis, tempore ex laboriosam, quibusdam, accusamus odit debitis cumque commodi fugiat?",
          open: false
        },
        {
          question: "The analysis",
          answer: "Tenetur odio veniam ut nobis, tempore ex laboriosam, quibusdam, accusamus odit debitis cumque commodi fugiat?",
          open: false
        }
      ]
    }
  },
  methods: {
    toggleOpen: function (index) {
      this.faqs = this.faqs.map((faq, i) => {
        if (index === i) {
          faq.open = !faq.open;
        } else {
          faq.open = false;
        }
        return faq;
      });
    }
  }
}
</script>
