<template>
  <div class="container">
    <div class="dropdown-container">
      <dropdown :dropdownItems="dropdownItems" @select-item="selectItem"></dropdown>
    </div>
    <div class="content-container">
      <div class="row">
        <div class="col-md-6 offset-md-3 text-center">
          <img src="@/assets/Sander-de-slaapapneu-patient.svg" alt="Character Image" class="img-fluid">
          <h3 class="card-title">{{ selectedItem.title }}</h3>
          <p class="card-text">{{ selectedItem.description }}</p>
          <button class="btn btn-primary">Play</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Dropdown from './Dropdown.vue';

export default {
  components: {
    Dropdown,
  },
  data() {
    return {
      dropdownItems: ['Bariatric Surgery', 'Sleep Apnea', 'Dementia'],
      selectedItem: {},
      items: [
        {
          value: 'option1',
          title: 'Bariatric Surgery',
          description: 'This is the description for Option 1.',
        },
        {
          value: 'option2',
          title: 'Sleep Apnea',
          description: 'This is the description for Option 2.',
        },
        {
          value: 'option3',
          title: 'Dementia',
          description: 'This is the description for Option 3.',
        },
      ],
    };
  },
  methods: {
    selectItem(item) {
      this.selectedItem = this.items[item];
    },
  },
};
</script>

<style scoped>
.container {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  background: linear-gradient(#0381B8, #0996AC, #0CBAA3, #08C492, #09B567);
}

.dropdown-container {
  margin-top: 1rem;
}

.content-container {
  flex: 1 0 auto;
  display: flex;
  align-items: center;
}

.card-title {
  font-size: 24px;
  margin-bottom: 1rem;
}

.card-text {
  font-size: 16px;
  margin-bottom: 1.5rem;
}

.btn-primary {
  padding: 0.5rem 1rem;
  font-size: 16px;
}
</style>
