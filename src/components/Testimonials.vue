<template>
  <div class="testimonials">
    <div class="testimonials__header">
      <GreenDivider/>
      <h1 class="testimonials__header-title">
        Lorem ipsum, dolor sit amet consectetur adipisicing elit.
      </h1>
    </div>
    <section class="testimonials__post-active">
      <img src="@/assets/avatar.png" alt="avatar" class="testimonials__post-active_avatar">
      <div class="testimonials__post-active-text">
        <img
          src="@/assets/lower_quotes.svg"
          alt=""
          class="testimonials__post-active-text_rightquote"
        >
        <img
          src="@/assets/upper_quotes.svg"
          alt=""
          class="testimonials__post-active-text_leftquote"
        >
        <p class="testimonials__posts-post_text">
          Lorem ipsum, dolor sit amet consectetur adipisicing elit. Laboriosam quas, aut
          consectetur animi  autem aliquid consequuntur suscipit exercitationem laborum cupiditate
          magnam eaque quae deleniti, iste nisi expedita, provident excepturi officia!Porro ab
          rerum omnis magnam eligendi error nobis dolore? Porro ab rerum omnis magnam eligendi
          error nobis dolore? Porro ab rerum omnis magnam eligendi error nobis dolore?
        </p>
        <h3>Jane Doe</h3>
      </div>
    </section>
    <div class="testimonials__posts">
      <section class="testimonials__posts-post">
        <div class="testimonials__posts-post_text">
          <p>
            Lorem ipsum, dolor sit amet consectetur adipisicing elit. Laboriosam quas, aut
            consectetur animi  autem aliquid
          </p>
          <h3>Jane Doe</h3>
        </div>
        <img src="@/assets/avatar.png" alt="avatar">

      </section>
      <section class="testimonials__posts-post">
        <img src="@/assets/avatar.png" alt="avatar">
        <div class="testimonials__posts-post_text">
          <p>
            Lorem ipsum, dolor sit amet consectetur adipisicing elit. Laboriosam quas, aut
            consectetur animi  autem aliquid
          </p>
          <h3>Jane Doe</h3>
        </div>
      </section>
    </div>
  </div>
</template>

<script>
import GreenDivider from '@/components/UI/GreenDivider.vue';

export default {
  name: 'TestimonialsSection',
  components: {
    GreenDivider,
  },

};
</script>

<style lang="scss" scoped>
.testimonials {
  color:$blue;
  padding: 4rem 4.5rem;
  display: flex;
  width: 53%;
  flex-direction: column;
  align-items: center;
  position: relative;
  @media screen and (max-width: 870px) {
    width: 100%;
  }
  &__header{
    position: absolute;
    top: 5rem;
    display: flex;
    flex-direction: column;
    align-items: center;
    &-title{
      font-size: 40px;
      font-weight: 700;
      text-align: center;
    }
  }
  &__post-active{
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-top: 10rem;
    margin-bottom: 1rem;
    @media screen and (max-width: 1100px){
      width: 120%;
    }
    @media screen and (max-width: 950px) {
      display: flex;
      justify-content: center;
      flex-direction: column;
      align-items: center;
      border-radius: 32px;
      border: 1px solid;
      margin-top: 13rem;
      border-image-source: linear-gradient(318.43deg,
        rgba(0, 195, 104, 0.4) 0%, rgba(0, 195, 104, 0) 99.05%);
      box-shadow: 0 8px 16px 0 #00C3683D;
      position: relative;
      padding-top: 6rem;
      &_avatar{
        position: absolute;
        top: -60px;
      }
    }
    @media screen and (max-width: 500px){
      margin-top: 16rem;
    }
    @media screen and (max-width: 371px){
      margin-top: 18rem;
    }
    &-text{
      position: relative;
      margin-left: 3rem;
      @media screen and (max-width: 950px) {
        font-size: 16px;
        text-align: center;
        margin: 1rem 0;
        &_leftquote{
          margin-top: -4.25rem;
          margin-left: 3.5rem;
        }
        &_rightquote{
          top: -6rem;
          padding-right: 1rem;
        }
      }
      &_leftquote{
        position: absolute;
        top: -0.5rem;
        left: -3rem;
        margin-right: 1rem;
      }
      &_rightquote{
        position: absolute;
        margin-top: 1rem;
        bottom: 0;
        right: 0;
      }
      h3{
        margin-top: 0.725rem;
      }
    }
    &_avatar{
      width: 187px;
      height: 187px;
    }
  }
  &__posts {
    display: flex;
    margin-top: 1rem;
    &-post{
      display: flex;
      justify-content: space-between;
      align-items: center;
      @media screen and (max-width: 1100px) {
        flex-direction: column;
        h3{
          margin-bottom: 0.5rem;
        }
      }
      &_text{
        font-size: 16px;
        font-weight: 400;
        margin-top: 0.5rem;
        h3{
          margin-top: 0.5rem;
        }
      }
    }
  }
}
</style>
