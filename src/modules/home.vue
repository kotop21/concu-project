<script setup lang="ts">
import {
  Card,
  CardContent,
  CardDescription,
  CardFooter,
  CardHeader,
  CardTitle,
} from '@/components/ui/card'
</script>

<template>
  <div data-tilt data-tilt-axis="y"  data-tilt-glare data-tilt-max-glare="0.06" data-tilt-full-page-listening>
    <Card class="shadow">
      <CardHeader>
        <CardTitle><h2>Головна</h2></CardTitle>
        <CardDescription> 
          Ласкаво просимо на наш сайт, присвячений неймовірним подорожам космічних апаратів "Вояджер-1" та "Вояджер-2"! Ці космічні кораблі є справжніми героями вивчення космосу і вже десятиліття служать нам як відкриттями, що змінюють наше розуміння всесвіту.
        </CardDescription>
      </CardHeader>
      <div class="horizontal-line"/>
      <CardContent>
        <br><h3>Вояджер-1: Перший Доплин до Невідомого</h3><br>
        "Вояджер-1" був запущений 5 вересня 1977 року і став першим апаратом, який пройшов через величезну простори космосу. Його головною метою було вивчення великої планети Юпітер і Сатурн, а також їхніх місяців. Апарат надав безцінні дані про атмосферу, структуру та магнітосферу цих гігантів, а його шлях веде його тепер до межі міжзорянного простору.<br>
        <br><h3>Вояджер-2: У Слід за Сусідом</h3><br>
        Апарат "Вояджер-2" вийшов на орбіту 20 серпня 1977 року і виконував схожі місії, обстежуючи Юпітер, Сатурн, Уран і Нептун. Цей апарат є єдиною космічною місією, яка досліджувала всі чотири великі газові гіганти нашої Сонячної системи. Зараз "Вояджер 2" також перебуває в межах міжзоряного простору, надсилаючи до нас важливі дані про міжзоряний простір.

        
      </CardContent>
    </Card>
  </div>
  <script src="https://cdn.jsdelivr.net/npm/vanilla-tilt@1.7.0/dist/vanilla-tilt.min.js"></script>
</template>

<style>

  .shadow{
    box-shadow: 5px 5px 50px 0px rgba(198, 198, 198, 0.04 );

  }

</style>