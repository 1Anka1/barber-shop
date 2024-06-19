<template>
  <section class="section">
    <div class="container about-barber_barber-content">
      <div class="about-barber_barber-details">
        <h1 class="about-barber_title">
          Cześć,
          <br />Mam na imię Ines!
        </h1>
        <p class="about-barber_information">
          Jestem doświadczonym barberem z wieloletnim doświadczeniem w strzyżeniu i stylizację
          brody. Jestem tutaj, aby podzielić się z Tobą moją wiedzą i umiejętnościami, ucząc Cię
          sztuki barberingu i stylizacji brody. Niezależnie od tego, czy jesteś początkującym, czy
          chcesz udoskonalić swoją technikę, cieszę się, że mogę poprowadzić Cię w tej podróży.
          Przekształćmy razem Twoją pasję w doświadczenie!
        </p>
        <div class="about-barber_button-wrapper">
          <button type="button" class="contact-button">Napisz do mnie</button>
        </div>
      </div>

      <div class="about-barber_barber-photo">
        <img src="../../../../../public/img/master.png" alt="Barber" width="550" height="690" />
      </div>
    </div>
  </section>
</template>

<style scoped>
.about-barber_barber-content {
  display: flex;
  gap: 100px;
}

.about-barber_barber-details {
  flex-direction: column;
  display: flex;
  gap: 35px;
}

.about-barber_button-wrapper {
  text-align: center;
}

.about-barber_title {
  font-family: var(--secondary-font);
  line-height: 1.3;
  font-size: 45px;
}

.about-barber_information {
  font-size: 21px;
  font-weight: 200;
  line-height: 2.2rem;
}

.contact-button {
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
}

.contact-button:hover {
  background-color: rgb(249, 250, 251);
}

.about-barber_barber-photo {
  position: relative;
  display: inline-block;
}

.about-barber_barber-photo img {
  display: block;
}

.about-barber_barber-photo::before,
.about-barber_barber-photo::after {
  position: absolute;
  box-sizing: border-box;
  z-index: 1;
}

.about-barber_barber-photo::before {
  content: url('../../../../../public/img/border-down.png');
  top: 86%;
}

.about-barber_barber-photo::after {
  content: url('../../../../../public/img/border-top.png');
  bottom: 88%;
}
</style>
