<script setup lang="ts">
import { Button } from '@/components/ui/button'
import { Eclipse } from 'lucide-vue-next'
import {
  Card,
  CardContent,
  CardDescription,
  CardFooter,
  CardHeader,
  CardTitle,
} from '@/components/ui/card'
import { Accordion, AccordionContent, AccordionItem, AccordionTrigger } from '@/components/ui/accordion'

</script>

<template>
  <div data-tilt-full-page-listening>
    <swiper-container
      class="mySwiper"
      scrollbar="true"
      direction="vertical"
      slides-per-view="auto"
      free-mode="true"
      mousewheel="true"
    >
      <swiper-slide>
        <Card class="" >
          <CardHeader>
            <CardTitle style="display: flex; align-items: center; height: 60px;"><Eclipse class="w-7 h-7"/><h2> Золота Платівка</h2></CardTitle>
            <CardDescription> 
              Піонери 10 і 11, які передували «Вояджеру», мали на собі невеликі металеві таблички, що вказували на час і місце їх походження, на користь будь-яких інших космонавтів, які могли б знайти їх у далекому майбутньому. Маючи перед собою цей приклад, НАСА розмістило більш амбітне повідомлення на борту «Вояджерів-1» і «Вояджерів-2», свого роду капсули часу, призначеної для того, щоб повідомити історію нашого світу інопланетянам. Повідомлення «Вояджера» передається на фонографічну платівку, 12-дюймовий позолочений мідний диск, що містить звуки та зображення, відібрані для зображення різноманітності життя та культури на Землі.
            </CardDescription>
          </CardHeader>
          <div class="horizontal-line"/>
          
          <CardContent>
                <Accordion type="single" collapsible>
                    <AccordionItem value="item-1">
                    <AccordionTrigger>Як прочитати Золоту платівку?</AccordionTrigger>
                    <AccordionContent>
                      Інформація у верхній правій частині обкладинки призначена для того, щоб показати, як зображення мають бути побудовані із записаних сигналів. Верхній малюнок показує типовий сигнал, який виникає на початку зображення. З цього сигналу створюється зображення, яке відтворює зображення у вигляді серії вертикальних ліній, подібно до звичайного телебачення (у якому зображення є серією горизонтальних ліній).
                      <br><br>Рядки зображення 1, 2 і 3 позначаються у двійкових числах, а також зазначається тривалість одного з «рядків зображення», приблизно 8 мілісекунд. Малюнок нижче показує:
                      <br>
                      <ul class="my-6 ml-6 list-disc [&>li]:mt-2">
                        <li>Як ці лінії малюватимуть вертикально, з переплетенням у шаховому порядку, щоб отримати правильну картинку.</li>
                        <li>Відразу під цим наведено креслення всього растру зображення, яке показує, що повне зображення складається з 512 вертикальних ліній.</li>
                        <li>Під цим є копія першого зображення в записі, щоб дозволити одержувачам перевірити, чи правильно вони декодують сигнали.</li>
                      </ul>
                      На цьому зображенні було використано коло, щоб переконатися, що реципієнти використовують правильне співвідношення горизонтальної та вертикальної висоти під час реконструкції зображення.
                      <br><br><img src="https://media.discordapp.net/attachments/854647157495824394/1206613205116522496/7.jpg?ex=65dca51d&is=65ca301d&hm=2cc00c6ae30cf8b9a3c712f9ec164f1b849f59479abc0ca9722978575a61afff&=&format=webp&width=1024&height=540"/>       
                    </AccordionContent>
                    </AccordionItem>
                </Accordion>
                <Accordion type="single" collapsible>
                    <AccordionItem value="item-1">
                    <AccordionTrigger>Який зміст Золотої платівки?</AccordionTrigger>
                    <AccordionContent>
                      Зміст запису було відібрано для NASA комітетом під головуванням Карла Сагана з Корнельського університету та інших вчених. Доктор Саган і його колеги зібрали 115 зображень і різні природні звуки, такі як звуки прибою, вітру та грому, птахів, китів та інших тварин. До цього вони додали музичні добірки з різних культур і епох, усні вітання від землян п’ятдесятьма п’ятьма мовами та друковані послання від президента Картера та генерального секретаря ООН Вальдхайма.
                      <br><br><blockquote class="mt-6 border-l-2 pl-6 italic">
                        «Космічний корабель буде зустрінутий і запис буде відтворений тільки в тому випадку, якщо в міжзоряному просторі існують розвинені космічні цивілізації»
                        <br><br>Карл Саган</blockquote><br><br>
Кожна платівка загорнута в захисну алюмінієву оболонку разом з картриджем і голкою. Інструкція символічною мовою пояснює походження космічного апарату та вказує, як відтворювати платівку. 115 зображень закодовані в аналоговій формі.
<br>
                    <br><img src="https://media.discordapp.net/attachments/854647157495824394/1206613204449501184/2.jpg?ex=65dca51d&is=65ca301d&hm=f17f64d28e8436718b7f42bc7f1e35fe4edae139c1443be3c397e383e95146b3&=&format=webp&width=1024&height=768"/>
                    Анатомія людської дитини
                    <img src="https://media.discordapp.net/attachments/854647157495824394/1206613205678428190/unnamed_2.gif?ex=65dca51e&is=65ca301e&hm=32b19706bfab93843d93d0500547be0930fd980c7188e1fecc05462f653d9792&=&width=1024&height=768"/>
                    Запуск ракети
                    <img src="https://media.discordapp.net/attachments/854647157495824394/1206613187261108304/unnamed_3.gif?ex=65dca519&is=65ca3019&hm=84c2e5cd4493aa286502b142c230fcd2a567b09fa4004201f1c402a781916917&=&width=1024&height=768"/>
                    Рентген людської руки
                    <img src="https://media.discordapp.net/attachments/854647157495824394/1206613187613556856/unnamed_4.gif?ex=65dca519&is=65ca3019&hm=cfdf9ba11a7ddb151dd0d27cfa71fb580d2e6110e4163565cc163e791d4c9bde&=&width=1024&height=768"/>
                    Людські діти та глобус
                    </AccordionContent>
                    </AccordionItem>
                </Accordion>
                <Accordion type="single" collapsible>
                    <AccordionItem value="item-1">
                    <AccordionTrigger>Створення Золотої платівки</AccordionTrigger>
                    <AccordionContent>
                      Багато людей брали участь у розробці, створенні та виготовленні золотої платівки. Чисті платівки були надані компанією Pyral S.A. з міста Крітей, Франція. CBS Records уклала контракт з Центром різання JVC у Боулдері, штат Колорадо, щоб вирізати лакові диски, які потім були відправлені до Центру обробки записів Джеймса Г. Лі у Гардені, штат Каліфорнія, щоб вирізати і позолотити вісім платівок Вояджера. Позолота була нанесена 23 серпня 1977 року, після чого платівки були змонтовані в алюмінієві контейнери і доставлені в JPL. <br><br>Платівка виготовлена з позолоченої міді і має діаметр 12 дюймів (30 см). Обкладинка платівки алюмінієва, на ній гальванічним способом нанесено надчистий зразок ізотопу урану-238. Період напіврозпаду урану-238 становить 4,468 мільярда років. На поверхні платівки також викарбувано вручну напис "Творцям музики - усім світам, усім часам".<br>
                    <br><img src="https://media.discordapp.net/attachments/854647157495824394/1206613194710192238/unnamed_8.jpg?ex=65dca51b&is=65ca301b&hm=fef20eb51ba27da87db2f218248772523253ff46f4080363ee251ced8deabff6&=&format=webp&width=1024&height=950"/>       
                    </AccordionContent>
                    </AccordionItem>
                </Accordion>
          </CardContent>
          
          <CardFooter>

          </CardFooter>
        </Card>
      </swiper-slide>
    </swiper-container>

  </div>
</template>

<style>

  .shadow{
    box-shadow: 5px 5px 50px 0px rgba(198, 198, 198, 0.04 );

  }

</style>