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
        <img src="@/assets/img/barber.png" alt="Barber" width="550" height="690" />
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
    gap: 45px;
  }

  &__wrapper-details {
    display: flex;
    flex-direction: column;
    gap: 35px;
  }

  &__title {
    font-family: var(--secondary-font);
    line-height: 1.3;
    font-size: 60px;

    @include breakpoint($screen-md) {
      font-size: 45px;
    }
  }

  &__information {
    font-size: 21px;
    font-weight: 200;
    line-height: 2.2rem;
  }

  &__wrapper-btn {
    text-align: center;
  }

  &__contact-btn {
    cursor: pointer;
    background-color: var(--primary-color);
    border: 0;
    border-radius: 1.5rem;
    font-size: 20px;
    font-weight: 200;
    line-height: 1.25rem;
    padding: 30px 70px;
    box-shadow:
      0 1px 3px 0 rgba(0, 0, 0, 0.1),
      0 1px 2px 0 rgba(0, 0, 0, 0.06);
    transition: background-color 250ms var(--timing-function);

    &:hover {
      background-color: rgb(249, 250, 251);
    }
  }

  &__barber-photo {
    position: relative;
    display: inline-block;

    &::before,
    &::after {
      position: absolute;
      box-sizing: border-box;
      z-index: 1;
    }

    &::before {
      content: url('@/assets/img/border-down.png');
      top: 86%;
    }

    &::after {
      content: url('@/assets/img/border-top.png');
      bottom: 89%;
      right: 0;
    }
  }
}
</style>
