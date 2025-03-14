<script setup>
import { Button } from '@/components/ui/button'
import { Book, Newspaper } from 'lucide-vue-next'
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
  const container = document.getElementById('module4');

  container.addEventListener('wheel', preventParentScroll);
  container.addEventListener('touchmove', preventParentScroll);
});

onBeforeUnmount(() => {
  const container = document.getElementById('module4');

  container.removeEventListener('wheel', preventParentScroll);
  container.removeEventListener('touchmove', preventParentScroll);
});

</script>

<template>
  <Card id="module4">
    <CardHeader>
      <CardTitle style="display: flex; align-items: center; ">
        <Newspaper class="w-7 h-7" />
        <h2> Новини</h2>
      </CardTitle>
    </CardHeader>
    <div class="horizontal-line" />
    <CardContent>
      <div class="element1" style="max-width: 100%;">
        <Accordion type="single" collapsible>
          <AccordionItem value="item-1">
            <AccordionTrigger>Voyager 1 почав надсилати на Землю рандомізовану інформацію з нулів та одиниць
            </AccordionTrigger>
            <AccordionContent>
              “Вояджер-1”, найвіддаленіший від Землі об’єкт, створений людиною, запущений майже 50 років тому,
              стикається
              з новим набором проблем зі зв’язком. Зонд, що знаходиться в даний час майже в 25 мільярдах кілометрів від
              Землі, посилає назад загадкові сигнали у вигляді незв’язаних двійкових послідовностей (нулів і одиниць).
              Значна відстань до “Вояджера-1”, через який час проходження сигналу становить більше 22 годин, ускладнює
              зусилля з виправлення цих аномалій. Навіть якщо функціональність “Вояджера-1” буде відновлена, час його
              роботи обмежений. Оскільки він виходить за межі хмар Оорта, потужності його передавача, ймовірно, буде
              недостатньо, щоб продовжувати надсилати сигнали назад на Землю. Цей виклик підкреслює складність глибокого
              космічного зв’язку та надзвичайну довговічність місій “Вояджер”, що значно перевищує їхні початкові
              очікування.<br>
            </AccordionContent>
          </AccordionItem>
        </Accordion>
        <Accordion type="single" collapsible>
          <AccordionItem value="item-1">
            <AccordionTrigger>Космічний аппарат «Вояджер-1» припинив передавати наукові дані на Землю</AccordionTrigger>
            <AccordionContent>
              «Вояджер-1» зараз знаходиться на відстані 162 рази віддаленій від Землі до Сонця. У минулому тижні
              відбувся
              збій одного з трьох бортових комп'ютерів, які обробляють команди з Землі. Це призвело до зависання
              телекомунікаційного блоку, відповідального за стан апарата та наукових інструментів. Науковці намагаються
              вирішити проблему, але це займе кілька тижнів. Команди місії тепер затримуються на шляху до «Вояджера-1»
              на
              22,5 години, і також настільки ж чекають на результат відновлення системи.<br>
            </AccordionContent>
          </AccordionItem>
        </Accordion>
        <Accordion type="single" collapsible>
          <AccordionItem value="item-1">
            <AccordionTrigger>NASA відновило сигнал із "Вояджером-2" після тижневої паузи</AccordionTrigger>
            <AccordionContent>
              Команда NASA зафіксувала сигнал від космічного апарата "Вояджер-2" після того, як тиждень тому втратила
              зв’язок через неправильно віддану команду. Зазначається, що команда місії була приємно здивована тим, що
              змогла виявити сигнал космічного зонда за допомогою міжнародного масиву радіоантен, які дозволяють NASA
              спілкуватися з місіями в усьому космосі.<br>
            </AccordionContent>
          </AccordionItem>
        </Accordion>
        <Accordion type="single" collapsible>
          <AccordionItem value="item-1">
            <AccordionTrigger>28 січня 2025 зонд Voyager 1 подолав символічну позначку, віддалившись на відстань у 25 млрд км від Землі.</AccordionTrigger>
            <AccordionContent>
              Про це свідчать дані трекера на сайті NASA, де вказується положення і швидкість апарата.
              28 січня він став першим космічним апаратом в історії, що віддалився на відстань 25 мільярдів кілометрів від нашої планети.
              Зараз випущеному із Землі сигналу потрібно 23 години та 9 хвилин, щоб дістатися до Voyager 1.
              Стільки ж потрібно на отримання відповіді від апарата. Важливо зазначити, що оскільки Земля обертається по орбіті навколо Сонця,
              через це в деякі моменти відстань між нашою планетою і Voyager 1 не збільшується, а скорочується.
              Що стосується Сонця, то зараз Voyager 1 перебуває на відстані 24,84 млрд км від нього.
              Апарат віддалиться від нашої зорі на дистанцію 25 млрд км у середині травня 2025 року.<br>
            </AccordionContent>
          </AccordionItem>
        </Accordion>
        <Accordion type="single" collapsible>
          <AccordionItem value="item-1">
            <AccordionTrigger>Наступною важливою віхою для Voyager 1 стане дистанція в один світловий день (25 902 068 371,2 км).</AccordionTrigger>
            <AccordionContent>
              Апарат віддалиться на таку відстань від Сонця в січні 2027 року — тобто в рік п’ятдесятиріччя свого запуску.
              Очікується, що до цього моменту Voyager 1 все ще буде функціонувати, хоча через виснаження ресурсу радіоізотопних генераторів інженерам,
              імовірно, доведеться відключити частину наукових інструментів, які у нього залишилися.<br>
            </AccordionContent>
          </AccordionItem>
        </Accordion>
      </div>
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
