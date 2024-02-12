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

onMounted(() => {
  const container = document.getElementById('module4'); // Замените 'your-container-id' на реальный идентификатор вашего контейнера
  container.addEventListener('wheel', preventParentScroll);
});

// Помните убрать внешний обработчик после уничтожения компонента
onBeforeUnmount(() => {
  const container = document.getElementById('module4');
  container.removeEventListener('wheel', preventParentScroll);
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
              <br><img
                src="https://media.discordapp.net/attachments/854647157495824394/1206613188486103060/unnamed_5.jpg?ex=65dca519&is=65ca3019&hm=3e51218bdaed115e7672dab62b78a7ed376259d54e93887daf034c795acd7d85&=&format=webp&width=816&height=1024" />
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
              <br><img
                src="https://media.discordapp.net/attachments/854647157495824394/1206613205376311316/unnamed_1.JPG?ex=65dca51d&is=65ca301d&hm=fe1418723c6ef6257a66607e1f555e5f4b895cd42618572bdeaf67c605859614&=&format=webp&width=1024&height=576" />
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
              <br><img
                src="https://media.discordapp.net/attachments/854647157495824394/1206613186908921938/unnamed_2.jpg?ex=65dca519&is=65ca3019&hm=5348d854cb9c567566666a9ebc678bf4b840a9f53215ec8e5a725a1ba16e7d93&=&format=webp&width=1024&height=576" />
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