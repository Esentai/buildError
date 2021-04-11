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
        <nb-title>Новости</nb-title>
      </nb-body>
      <nb-right />
    </nb-header>
    <nb-content padder>
      <nb-card>
        <nb-card-item>
          <nb-left>
            <nb-thumbnail :source="logo"></nb-thumbnail>
            <nb-body>
              <nb-text>Казтекбаев Азилхан</nb-text>
              <nb-text note>КСК "ЖК Гаухартас"</nb-text>
            </nb-body>
          </nb-left>
        </nb-card-item>

        <nb-card-item cardBody>
          <!-- <image
            :source="cardImage"
            class="card-item-image"
            :style="stylesObj.cardItemImage"
          /> -->
          <Text :style="{paddingLeft:15, paddingRight:15 }">
            15.04.2021 Будет сообрание по поводу сортировки мусора
            Уважаемые жители, мы хотим объявить собрание насчет сборки мусора, 
            чтобы сохранить экологию Казахстана, вы можете нам с этим помочь, и получить за это еще и бонусы.
          </Text>
        </nb-card-item>

        <nb-card-item>
          <nb-left>
            <nb-button transparent>
              <nb-icon name="thumbs-up" active></nb-icon>
              <nb-text>65 лайков</nb-text>
            </nb-button>
          </nb-left>
          <nb-right>
            <nb-text>5h ago</nb-text>
          </nb-right>
        </nb-card-item>
      </nb-card>
       <nb-card>
        <nb-card-item>
          <nb-left>
            <nb-thumbnail :source="logo"></nb-thumbnail>
            <nb-body>
              <nb-text>Казтекбаев Азилхан</nb-text>
              <nb-text note>КСК "ЖК Гаухартас"</nb-text>
            </nb-body>
          </nb-left>
        </nb-card-item>

        <nb-card-item cardBody>
          <image
            :source="cardImage"
            class="card-item-image"
            :style="stylesObj.cardItemImage"
          />
          <!-- <Text :style="{paddingLeft:15, paddingRight:15 }">
            15.04.2021 Будет сообрание по поводу организации мусора
            Увожаемые жители, мы хотим объявить собрание насчет сборки мусора, 
            чтобы сохранить экологию казахстана, вы можете нам с этим помочь и получить за это еще и бонусы
          </Text> -->
        </nb-card-item>

        <nb-card-item>
          <nb-left>
            <nb-button transparent>
              <nb-icon name="thumbs-up" active></nb-icon>
              <nb-text>70 лайков</nb-text>
            </nb-button>
          </nb-left>
          <nb-right>
            <nb-text>11h ago</nb-text>
          </nb-right>
        </nb-card-item>
      </nb-card>
       <nb-card>
        <nb-card-item>
          <nb-left>
            <nb-thumbnail :source="logo"></nb-thumbnail>
            <nb-body>
              <nb-text>Казтекбаев Азилхан</nb-text>
              <nb-text note>Администрация "ЖК Гаухартас"</nb-text>
            </nb-body>
          </nb-left>
        </nb-card-item>

        <nb-card-item cardBody>
          <!-- <image
            :source="cardImage"
            class="card-item-image"
            :style="stylesObj.cardItemImage"
          /> -->
          <Text :style="{paddingLeft:15, paddingRight:15 }">
            Что происходит с жилым комплексом, в котором мы живём? За повседневными делами и заботами, домашними хлопотами, занятиями спортом и многим другим у нас не остается времени задуматься об этом. А ведь от этого во многом зависит наш домашний комфорт и уют. ⠀
          </Text>
        </nb-card-item>

        <nb-card-item>
          <nb-left>
            <nb-button transparent>
              <nb-icon name="thumbs-up" active></nb-icon>
              <nb-text>56 лайков</nb-text>
            </nb-button>
          </nb-left>
          <nb-right>
            <nb-text>23 ago</nb-text>
          </nb-right>
        </nb-card-item>
      </nb-card>
    </nb-content>
  </nb-container>
</template>

<script>

import logo from "../../../assets/logo.png";
import cardImage from "../../../assets/news.jpg";

export default {
  
  data() {
    return {
      logo,
      cardImage,
      stylesObj: {
        cardItemImage: {
          resizeMode: "cover"
        }
      },
      listItemArr: [
        {
          route: "BasicCard",
          text: "Basic Card"
        },
        {
          route: "NHCardHeaderAndFooter",
          text: "Card Header & Footer"
        },
        {
          route: "NHCardItemBordered",
          text: "Bordered CardItem"
        },
        {
          route: "NHCardTransparent",
          text: "Transparent Card"
        },
        {
          route: "NHCardItemButton",
          text: "Button CardItem"
        },
        {
          route: "NHCardList",
          text: "Card List"
        },
        {
          route: "NHCardImage",
          text: "Card Image"
        },
        {
          route: "NHCardShowcase",
          text: "Card Showcase"
        }
      ]
    };
  }
};
</script>

<style>
.body-icon-color {
  color: #999;
}
.mb-15 {
  margin-bottom: 15;
}
.card-item-image {
  flex: 1;
  height: 200;
}
</style>
