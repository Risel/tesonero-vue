<template>
  <div class="faq">
    <div class="faq__header">
      <GreenDivider/>
      <h1 class="faq__header-title">Lorem ipsum, dolor sit adipisicing elit.</h1>
      <p class="faq__header-subtitle">Porro ab rerum omnis magnam eligendi error nobis dolore?</p>
    </div>
    <section class="faq__section">
      <Dropdown class="faq__section-items" v-for="item in items" :key="item.id" :id="item.id"
                :icon="item.icon" :title="item.title" :body="item.body" :isActive="item.isActive"
                @toggle-dropdown="handleToggle" />
    </section>
  </div>
</template>

<script>
import Dropdown from '@/components/Dropdown.vue';
import Joystick from '@/assets/stability24_icon.svg';
import LED from '@/assets/LED.svg';
import LightsOff from '@/assets/lights_off.svg';
import Splitter from '@/assets/splitter.svg';
import PowerOff from '@/assets/power_off.svg';
import GreenDivider from '@/components/UI/GreenDivider.vue';

export default {
  name: 'FAQ-footer',
  components: {
    GreenDivider,
    Dropdown,
  },
  data() {
    return ({
      items: [
        {
          id: 0,
          isActive: true,
          icon: Joystick,
          title: 'Lorem ipsum, dolor sit amet adipisicing elit.',
          body: 'Laboriosam quas, aut consectetur animi autem aliquid '
            + 'consequuntur suscipit exercitationem laborum cupiditate magnam eaque quae delenit',
        },
        {
          id: 1,
          isActive: false,
          icon: LED,
          title: 'Lorem ipsum, dolor sit amet adipisicing elit.',
          body: 'Laboriosam quas, aut consectetur animi autem aliquid consequuntur suscipit'
              + ' exercitationem laborum cupiditate magnam eaque quae delenit',
        },
        {
          id: 2,
          isActive: false,
          icon: LightsOff,
          title: 'Lorem ipsum, dolor sit amet adipisicing elit.',
          body: 'Laboriosam quas, aut consectetur animi autem aliquid consequuntur suscipit'
              + ' exercitationem laborum cupiditate magnam eaque quae delenit',
        },
        {
          id: 3,
          isActive: false,
          icon: Splitter,
          title: 'Lorem ipsum, dolor sit amet adipisicing elit.',
          body: 'Laboriosam quas, aut consectetur animi autem aliquid consequuntur suscipit '
              + 'exercitationem laborum cupiditate magnam eaque quae delenit',
        },
        {
          id: 4,
          isActive: false,
          icon: PowerOff,
          title: 'Lorem ipsum, dolor sit amet adipisicing elit.',
          body: 'Laboriosam quas, aut consectetur animi autem aliquid consequuntur suscipit '
              + 'exercitationem laborum cupiditate magnam eaque quae delenit',
        },
      ],
    });
  },
  methods: {
    handleToggle(id) {
      /* eslint-disable-next-line */
      for (const item of this.items) {
        if (item.id === id) {
          item.isActive = !item.isActive;
        } else {
          item.isActive = false;
        }
      }
    },
  },
};

</script>

<style lang="scss" scoped>
.faq {
  display: flex;
  align-items: center;
  flex-direction: column;
  width: 47%;
  background-color: #fff;
  padding: 4rem;
  color: $blue;
  @media screen and (max-width: 950px) {
    width: 100%;
    padding: 5rem 0.75rem;
  }
  &__header{
    position: absolute;
    top: 5rem;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 0 1rem;
    text-align: center;
    &-title{
      font-size: 40px;
      font-weight: 700;
      text-align: center;
      padding-bottom: 1rem;
    }
    &-subtitle{
      font-size: 16px;
      font-weight: 400;
    }
  }
  &__section{
    margin-top: 10rem;
    :hover{
      background-color: rgba(244, 244, 244, 0.7);
    }
    @media screen and (max-width: 950px) {
      margin-top: 11rem;
      width: 100%;
    }
    @media screen and (max-width: 380px) {
      margin-top: 13rem;
      width: 100%;
    }
  }
}
</style>
