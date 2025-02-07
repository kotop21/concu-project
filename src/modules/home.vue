<script setup>
import { Button } from '@/components/ui/button'
import { Home, ScanEye } from 'lucide-vue-next'
import {
  Card,
  CardContent,
  CardDescription,
  CardFooter,
  CardHeader,
  CardTitle,
} from '@/components/ui/card'
import {
  Dialog,
  DialogContent,
  DialogDescription,
  DialogFooter,
  DialogHeader,
  DialogTitle,
  DialogTrigger,
} from '@/components/ui/dialog'
import { onMounted, onBeforeUnmount } from 'vue';

const preventParentScroll = (event) => {
  event.stopPropagation();
};

const handleTouch = (event) => {
  event.preventDefault();
  event.stopPropagation();
};

onMounted(() => {
  const container = document.getElementById('module');

  container.addEventListener('wheel', preventParentScroll);
  container.addEventListener('touchmove', preventParentScroll);
});

onBeforeUnmount(() => {
  const container = document.getElementById('module');

  container.removeEventListener('wheel', preventParentScroll);
  container.removeEventListener('touchmove', preventParentScroll);
});

</script>


<template>
  <Card id="module">
    <CardHeader>
      <CardTitle style="display: flex; align-items: center; height: 60px;">
        <Home class="w-7 h-7" />
        <h2 class="text-3xl">Головна</h2>
      </CardTitle>
      <CardDescription style="font-size: 22px">
        Ласкаво просимо на наш сайт, присвячений неймовірним подорожам космічних апаратів "Вояджер-1" та
        "Вояджер-2"! Ці космічні кораблі є справжніми героями вивчення космосу і вже десятиліття служать нам як
        відкриттями, що змінюють наше розуміння всесвіту.
      </CardDescription>
    </CardHeader>
<div class="flex gap-5 mt-5">
  <figure class="flex-1">
    <img
      src="https://cdn.discordapp.com/attachments/1337518454642708500/1337518776324722750/5a78befa-96f4-4f55-9f4d-573ce1eba08f_cx0_cy14_cw0_w1080_h608_s.jpg?ex=67a7bcee&is=67a66b6e&hm=aba17e26b8eb9df7f5387195eca7d4c9c8cf11f0757c89a61a2d137357aef3e2&"
      alt="Вояджер-1"
      class="w-full h-48 object-cover rounded-lg"
    />
    <figcaption class="text-center mt-2 text-sm text-gray-600">Вояджер-1</figcaption>
  </figure>
  <figure class="flex-1">
    <img
      src="https://cdn.discordapp.com/attachments/1337518454642708500/1337519027244761139/image-625-1693386682.6599.jpg?ex=67a7bd29&is=67a66ba9&hm=632ef0c4f8705445567c7d86b63911495623feddaa77cfcfe4bfd019fb040ac8&"
      alt="Вояджер-2"
      class="w-full h-48 object-cover rounded-lg"
    />
    <figcaption class="text-center mt-2 text-sm text-gray-600">Вояджер-2</figcaption>
  </figure>
</div>
    <div class="horizontal-line" />

    <CardContent>
      <br><b>
        <h3 class="text-2xl">Вояджер-1: Перший Доплин до Невідомого</h3>
      </b><br>
      <h4 class="text-lg">"Вояджер-1" був запущений 5 вересня 1977 року і став першим апаратом, який пройшов через величезну
        простори космосу. Його головною метою було вивчення великої планети Юпітер і Сатурн, а також їхніх місяців.
        Апарат надав безцінні дані про атмосферу, структуру та магнітосферу цих гігантів, а його шлях веде його
        тепер до межі міжзорянного простору.<br>
        <br><b>
          <h3>Вояджер-2: У Слід за Сусідом</h3>
        </b><br>
        Апарат "Вояджер-2" вийшов на орбіту 20 серпня 1977 року і виконував схожі місії, обстежуючи Юпітер, Сатурн,
        Уран і Нептун. Цей апарат є єдиною космічною місією, яка досліджувала всі чотири великі газові гіганти нашої
        Сонячної системи. Зараз "Вояджер 2" також перебуває в межах міжзоряного простору, надсилаючи до нас важливі
        дані про міжзоряний простір.
      </h4>

    </CardContent>

    <CardFooter>
      <Dialog>
        <DialogTrigger>
          <Button class="ml-auto">
            <ScanEye />Вояджер в 3д
          </Button>
        </DialogTrigger>
        <DialogContent>
          <DialogHeader>
            <DialogDescription>
              <spline-viewer loading-anim-type="spinner-small-dark"
                url="https://prod.spline.design/g1SVp-qo1HRHUk14/scene.splinecode"></spline-viewer>
            </DialogDescription>
          </DialogHeader>
        </DialogContent>
      </Dialog>
    </CardFooter>
  </Card>
</template>

<style>

.shadow {
  box-shadow: 5px 5px 50px 0px rgba(198, 198, 198, 0.04);

}
</style>
