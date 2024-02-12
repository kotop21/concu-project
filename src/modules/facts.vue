<script setup>
import { Button } from '@/components/ui/button'
import { Lightbulb, Newspaper } from 'lucide-vue-next'
import {
  Card,
  CardContent,
  CardDescription,
  CardFooter,
  CardHeader,
  CardTitle,
} from '@/components/ui/card'
import { Accordion, AccordionContent, AccordionItem, AccordionTrigger } from '@/components/ui/accordion'
import { onMounted, onBeforeUnmount } from 'vue';

const preventParentScroll = (event) => {
  event.stopPropagation();
};

const handleTouch = (event) => {
  event.preventDefault();
  event.stopPropagation();
};

onMounted(() => {
  const container = document.getElementById('module5');

  container.addEventListener('wheel', preventParentScroll);
  container.addEventListener('touchmove', preventParentScroll);
});

onBeforeUnmount(() => {
  const container = document.getElementById('module5');

  container.removeEventListener('wheel', preventParentScroll);
  container.removeEventListener('touchmove', preventParentScroll);
});

</script>

<template>
  <Card id="module5">
    <CardHeader>
      <CardTitle style="display: flex; align-items: center; ">
        <Lightbulb class="w-7 h-7" />
        <h2> Цікаві факти</h2>
      </CardTitle>
    </CardHeader>
    <div class="horizontal-line" />
    <CardContent>
      <ul class="my-6 ml-6 list-disc [&>li]:mt-2">
        <li>Станом на жовтень 2022 року «Вояджер-1» — найвіддаленіший від Землі об'єкт, створений людством. Він
          знаходиться на відстані 158,25 астрономічної одиниці, або 23,674 млрд км. </li>
        <li>«Вояджер-1» насправді було запущено пізніше «Вояджера-2», який стартував у липні 1979, тоді як «Вояджер-1»
          було запущено тільки у вересні 1979 року. Але траєкторії апаратів були побудовані так, що саме «Вояджер-1»
          першим діставався більшості цікавих об'єктів. </li>
        <li>17 лютого 1998-го "Вояджер-1" на відстані 10,4 млрд км від Землі обігнав апарат "Піонер-10". Апарат летить
          зі
          швидкістю близько 60 тис. км/год.</li>
        <li>На золотій пластині записали вітання на 55 мовах світу. Там також записана класична музика, звуки природи,
          зображення людей і тварин. На пластині зберігаються координати Землі та Сонячної системи.</li>
        <li>Якщо продовжить свою роботу, Вояджер 1 може потрапити в міжзоряний простір близько 40 000 років після
          запуску,
          а Вояджер 2 - через приблизно 296 000 років</li>
        <li>Вояджер 1 виявив незвичайний об'єкт на Сатурні, відомий як "Велика Темна Пляма". Це загадкове утворення
          з'явилося в 1980 році та ще досі викликає науковий інтерес.</li>
      </ul>
    </CardContent>
  </Card>
</template>

<style>
img {
  display: block;
  margin: auto;
}

.element1 {
  max-width: 100%;
}

.shadow {
  box-shadow: 5px 5px 50px 0px rgba(198, 198, 198, 0.04);

}
</style>