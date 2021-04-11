<template>
  <nb-container :style="{ backgroundColor: '#fff' }">
    <nb-header>
      <nb-left>
        <nb-button
          transparent
          :onPress="() => this.props.navigation.openDrawer()"
        >
          <nb-icon name="menu" />
        </nb-button>
      </nb-left>
      <nb-body>
        <nb-title>Переработка</nb-title>
      </nb-body>
      <nb-right />
    </nb-header>
  
    <nb-tabs :renderTabBar="getScollableTabComp">
      <nb-tab heading="Бонусы">
        <tab-one />
      </nb-tab>
      <nb-tab heading="Расписания">
        <tab-two />
      </nb-tab>
      <nb-tab heading="Статистика">
        <tab-three />
      </nb-tab>
      <nb-tab heading="Информация">
        <tab-four />
      </nb-tab>
    </nb-tabs>
  </nb-container>
</template>

<script>

import React from "react";
import { ScrollableTab } from "native-base";
import TabOne from "./components/tabOne";
import TabTwo from "./components/tabTwo";
import TabThree from "./components/tabThree";
import TabFour from "./components/tabFour";
import TabFive from "./components/tabFive";

export default {
  components: { TabOne, TabTwo, TabThree, TabFour, TabFive },
  data() {
    return {
      listItemArr: [
        {
          route: "BasicTab",
          text: "Basic Tabs"
        },
        {
          route: "ConfigTab",
          text: "Advanced Tabs"
        },
        {
          route: "ScrollableTab",
          text: "Scrollable Tabs"
        }
      ]
    };
  },
    methods: {
    getScollableTabComp() {
      return <ScrollableTab />;
    }
  }
};
</script>

<style>
.body-icon-color {
  color: #999;
}
</style>
