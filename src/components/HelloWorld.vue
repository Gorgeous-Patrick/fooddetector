<template>
  <v-container>
    <v-row justify="center" class="text-center">
      <v-col cols="12">
        <v-img
          :src="require('../assets/logo.jpg')"
          class="my-3"
          contain
          height="200"
        />
      </v-col>

      <v-col class="mb-4" cols="12">
        <h1 class="display-2 font-weight-bold mb-3">JI Dorm Book</h1>
      </v-col>
      <v-col cols="11" sm="3">
      <v-text-field label="姓名 Name" outlined></v-text-field>
      </v-col>
      <v-col cols="11" sm="3">
      <v-text-field label="宿舍楼 Building" outlined></v-text-field>
      </v-col>
      <v-col cols="11" sm="3">
      <v-text-field label="寝室号 Room" outlined></v-text-field>
      </v-col>

      

      <v-col cols="12">
        <h3>早餐 Breakfast</h3>
      </v-col>
      <v-col cols="11" sm="4" class="mb-5">
        <v-select
          v-model="selectBreakfast"
          :items="items"
          item-text="state"
          item-value="abbr"
          label="Breakfast"
          persistent-hint
          return-object
          single-line
        ></v-select>
      </v-col>
      <v-col cols="12">
        <h3>中餐 Lunch</h3>
      </v-col>
      <v-col cols="11" sm="4" class="mb-5">
        <v-select
          v-model="selectLunch"
          :items="items"
          item-text="state"
          item-value="abbr"
          label="Lunch"
          persistent-hint
          return-object
          single-line
        ></v-select>
      </v-col>
      <v-col cols="12">
        <h3>晚餐 Dinner</h3>
      </v-col>
      <v-col cols="11" sm="4" class="mb-5">
        <v-select
          v-model="selectDinner"
          :items="items"
          item-text="state"
          item-value="abbr"
          label="Dinner"
          persistent-hint
          return-object
          single-line
        ></v-select>
      </v-col>
      <v-col cols="12" sm="12" class="mb-5">
        <v-btn elevation="2" color="primary" @click="submit">提交 Submit</v-btn>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "HelloWorld",

  data: () => ({
    selectBreakfast: { state: "不要 No need", abbr: "no" },
    selectLunch: { state: "不要 No need", abbr: "no" },
    selectDinner: { state: "不要 No need", abbr: "no" },
    items: [
      { state: "不要 No need", abbr: "no" },
      { state: "普通 Normal", abbr: "normal" },
      { state: "普通2份 Double sized normal", abbr: "normalDouble" },
      { state: "清真 Muslim cuisine", abbr: "muslim" },
      { state: "清真2份 Double sized muslim cuisine", abbr: "muslimDouble" },
    ],
  }),
  methods: {
    submit() {
      console.log(this.selectBreakfast.abbr);
      return;
    },
  },
};
</script>
