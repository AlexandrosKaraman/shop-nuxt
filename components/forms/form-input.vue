<template>
  <div>
    <form class="form" @submit.prevent="submit">
      <div class="form__title">Обратная связь</div>
      <div class="form__item">
        <div
          class="form-group"
          :class="{ 'form-group--error': $v.name.$error }"
        >
          <input
            class="form__name"
            placeholder="Имя*"
            v-model.trim="name"
            @input="setName($event.target.value)"
          />
        </div>
        <div class="error" v-if="$v.name.$dirty && !$v.name.required">
          Необходимо заполнить поле Имя
        </div>
        <div class="error" v-if="!$v.name.minLength">
          Имя должно иметь не менее {{ $v.name.$params.minLength.min }} букв.
        </div>
      </div>

      <div class="form__item">
        <div
          class="form-group"
          :class="{ 'form-group--error': $v.email.$error }"
        >
          <input
            class="form__name"
            placeholder="Ваша почта*"
            v-model.trim="email"
            @input="setEmail($event.target.value)"
          />
        </div>
        <div class="error" v-if="$v.email.$dirty && !$v.email.required">
          Не верно заполнено поле Email
        </div>
      </div>

      <div class="form__item">
        <div
          class="form-group"
          :class="{ 'form-group--error': $v.question.$error }"
        >
          <input
            class="form__input"
            placeholder="Ваш вопрос, отзыв или пожелание*"
            v-model.trim="question"
            @input="setQuestion($event.target.value)"
          />
        </div>
        <div class="error" v-if="$v.question.$dirty && !$v.question.required">
          Пожалуйста, введите сообщение
        </div>
        <div class="error" v-if="!$v.question.minLength">
          Сообщение должно иметь не менее
          {{ $v.question.$params.minLength.min }} букв.
        </div>
      </div>

      <div class="form__item">
        <input
          class="form-input__checkbox"
          type="checkbox"
          v-model="agreeCheckBox"
        />
        <label for="notification">
          Настоящим подтверждаю, что я ознакомлен и согласен с условиями оферты
          и политики конфиденциальности *</label
        >
      </div>
      <div class="form__item">
        <button
          class="form__button"
          type="submit"
          :disabled="submitStatus === 'PENDING'"
        >
          Отправить!
        </button>
        <p class="typo__p" v-if="submitStatus === 'OK'">Спасибо за заявку!</p>
        <p class="error" v-if="submitStatus === 'ERROR'">
          Пожалуйста, заполните форму правильно.
        </p>
        <p class="typo__p" v-if="submitStatus === 'PENDING'">Загрузка...</p>
      </div>
    </form>
  </div>
</template>

<script>
import { required, minLength, email } from "vuelidate/lib/validators";
import { validationMixin } from "vuelidate";

export default {
  mixins: [validationMixin],
  data() {
    return {
      name: "",
      email: "",
      question: "",
      agreeCheckBox: false,
      submitStatus: null,
    };
  },
  validations: {
    name: {
      required,
      minLength: minLength(4),
    },
    email: {
      required,
      email,
    },
    question: {
      required,
      minLength: minLength(10),
    },
  },

  methods: {
    setName(value) {
      this.name = value;
      this.$v.name.$touch();
    },
    setEmail(value) {
      this.email = value;
      this.$v.email.$touch();
    },
    setQuestion(value) {
      this.question = value;
      this.$v.question.$touch();
    },
    submit() {
      console.log("submit!");
      this.$v.$touch();
      if (this.$v.$invalid) {
        this.submitStatus = "ERROR";
      } else {
        // do your submit logic here
      }
    },
  },
};
</script>

<style lang="scss" scoped>
.form {
  max-width: 680px;

  display: grid;
  grid-template-columns: 5fr 5fr;
  grid-template-rows: 30px 100px 90px 45px 25px;
  justify-items: center;
  align-items: center;
  margin: 0 auto;
  row-gap: 20px;

  padding-top: 50px;

  &__name {
    width: 324px;
    height: 50px;
  }

  &__title {
    grid-column: 1/3;

    font-size: 30px;
    font-weight: 600;
  }

  &__input {
    width: 680px;
    height: 115px;
  }
  &__item:nth-child(2) {
    grid-column: 1/2;
    padding-right: 20px;
  }
  &__item:nth-child(3) {
    grid-column: 2/3;
  }
  &__item:nth-child(4) {
    grid-column: 1/3;
  }
  &__item:nth-child(5) {
    grid-column: 1/3;
  }
  &__item:nth-child(6) {
    grid-column: 1/3;
  }
  &__button {
    width: 221px;
    height: 40px;
    margin: 7px;
    color: rgba(255, 255, 255, 1);
    background-color: #1f7d63;
    border: none;
    border-radius: 5px;
    font-size: 17px;
    cursor: pointer;
  }
}
.error {
  color: red;
}
</style>