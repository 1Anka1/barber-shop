<script>
import { VueWriter } from 'vue-writer';
export default {
  components: { VueWriter },
};
</script>

<template>
  <section class="about-barber section">
    <div class="container about-barber__container">
      <div class="about-barber__wrapper-details">
        <h1 class="about-barber__title">
          <VueWriter :array="['Cześć, ']" :typeSpeed="70" :iterations="1" />
          <VueWriter :array="['Mam na imię Ines!']" :typeSpeed="70" :start="600" :iterations="1" />
        </h1>
        <p class="about-barber__information">
          Jestem doświadczonym barberem z wieloletnim doświadczeniem w strzyżeniu i stylizację
          brody. Jestem tutaj, aby podzielić się z Tobą moją wiedzą i umiejętnościami, ucząc Cię
          sztuki barberingu i stylizacji brody. Niezależnie od tego, czy jesteś początkującym, czy
          chcesz udoskonalić swoją technikę, cieszę się, że mogę poprowadzić Cię w tej podróży.
          Przekształćmy razem Twoją pasję w doświadczenie!
        </p>
        <div class="about-barber__wrapper-btn">
          <a href="https://t.me/Ines2259" target="_blank">
            <button type="button" class="about-barber__contact-btn">Napisz do mnie</button></a
          >
        </div>
      </div>
      <div class="about-barber__barber-photo">
        <img src="@/assets/img/barber.png" alt="Barber" />
      </div>
    </div>
  </section>
</template>

<style scoped lang="scss">
.about-barber {
  &__container {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 20px;

    @include breakpoint($screen-sm) {
      gap: 45px;
    }

    @include breakpoint($screen-lg) {
      display: grid;
      gap: 130px;
      grid-template-columns: repeat(2, 1fr);
      align-items: center;
    }
  }

  &__wrapper-details {
    display: flex;
    flex-direction: column;
    gap: 40px;
  }

  &__title {
    font-family: var(--secondary-font);
    line-height: 1.3;
    font-size: 45px;

    @include breakpoint($screen-md) {
      font-size: 45px;
    }
  }

  &__information {
    font-size: 15px;
    font-weight: 200;
    line-height: 1.5rem;

    @include breakpoint($screen-md) {
      font-size: 20px;
      line-height: 2.2rem;
    }
  }

  &__wrapper-btn {
    text-align: center;
  }

  &__contact-btn {
    cursor: pointer;
    background-color: var(--primary-color);
    border: 0;
    border-radius: 1.5rem;
    font-weight: 200;
    font-size: 15px;
    padding: 25px;

    box-shadow:
      0 1px 3px 0 rgba(0, 0, 0, 0.1),
      0 1px 2px 0 rgba(0, 0, 0, 0.06);
    transition: background-color 250ms var(--timing-function);

    @include breakpoint($screen-md) {
      font-size: 20px;
      line-height: 1.25rem;
      padding: 30px 70px;
    }

    &:hover {
      background-color: rgb(249, 250, 251);
    }
  }

  &__barber-photo {
    display: grid;
    position: relative;
    overflow: hidden;
    place-items: center;
    width: 100%;
    max-width: 550px;

    &::before,
    &::after {
      position: absolute;
      box-sizing: border-box;
      z-index: 1;
      width: 100%;
      height: auto;
    }

    &::before {
      content: url('@/assets/img/border-down.png');
      bottom: -10px;
      left: 0;
    }

    &::after {
      content: url('@/assets/img/border-top.png');
      top: -10px;
      left: 0;
    }
  }
}
</style>
