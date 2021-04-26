<template>
  <div>
    <h1>Отзывы клиентов</h1>
    <div class="feedback">
      <div class="feedback__item">
        <div class="feedback__title">Alexey</div>
        <div class="feedback__content">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Modi illo
          cupiditate ipsum, expedita voluptatem iusto esse quidem voluptates in
          dolore optio reprehenderit quia saepe porro, sunt excepturi, itaque
          repellendus rerum? sunt excepturi, itaque repellendus rerum?
        </div>
      </div>

      <div class="feedback__item">
        <div class="feedback__title">Sasha</div>
        <div class="feedback__content">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Modi illo
          cupiditate ipsum, expedita voluptatem iusto esse quidem voluptates in
          dolore optio reprehenderit quia saepe porro, sunt excepturi, itaque
          repellendus rerum? sunt excepturi, itaque repellendus rerum?
        </div>
      </div>

      <div class="feedback__item">
        <div class="feedback__title">Vasya</div>
        <div class="feedback__content">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Modi illo
          cupiditate ipsum, expedita voluptatem iusto esse quidem voluptates in
          dolore optio reprehenderit quia saepe porro, sunt excepturi, itaque
          repellendus rerum? sunt excepturi, itaque repellendus rerum?
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>



<style lang="scss" scoped>
h1 {
  margin: 70px 0px 40px 0px;
}

.feedback {
  display: grid;
  grid-template-columns: 3fr 3fr 3fr;

  &__item {
    width: 448px;
    height: 100%;

    background-color: #f3f2f2;
    border-radius: 10px;
  }
  &__title {
    font-size: 30px;
    font-weight: 600;

    padding: 20px 20px 0px 20px;
  }
  &__content {
    font-size: 24px;

    padding: 20px;
  }
}
@media (max-width: 767px) {
  .feedback {
    display: grid;
    grid-template-columns: 1fr;
    max-width: 767px;
    gap: 10px;
    justify-items: center;
  }
}
</style>