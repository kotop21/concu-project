Ocean World: Eden Crafters Prologue<script setup>
import { Button } from '@/components/ui/button'
import { Home, ScanEye, Book, Eclipse } from 'lucide-vue-next'
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
  const container = document.getElementById('module3');

  container.addEventListener('wheel', preventParentScroll);
  container.addEventListener('touchmove', preventParentScroll);
});

onBeforeUnmount(() => {
  const container = document.getElementById('module3');

  container.removeEventListener('wheel', preventParentScroll);
  container.removeEventListener('touchmove', preventParentScroll);
});

</script>

<template>
  <Card id="module3">
    <CardHeader>
      <CardTitle style="display: flex; align-items: center; height: 60px;">
        <Book class="w-7 h-7" />
        <h2> Історія</h2>
      </CardTitle>
      </CardHeader>
    <div>
      <h4 class="text-lg">Місія «Вояджерів», запланована на 4 роки, перевищила всі очікування вчених,
        і зараз космічне агентство вживає заходів для подовження їхнього функціонування.
        Однак останні звіти вказують на те, що подорож зондів-близнюків наближається до завершення:
        один з них почав надсилати помилкові дані через несправність обладнання, а із другим втрачено зв'язок через неправильні команди.
        Незважаючи на це, 46-річна місія «мандрівників» в космосі виявилася надзвичайно продуктивною.</h4>
    </div>
    <div class="horizontal-line" />
    <CardContent class="cont">
      <div class="container1">
        <br><b>
          <h3>Юпітер</h3>
        </b><br>
        <h4 class="text-wrap; text-lg" style="width: 6rem;">Зонди були створені з метою дослідження Юпітера та Сатурна, і перший з них досяг Юпітера у 1979 році.
          Проходячи повз цю планету, «Вояджер-1» і «Вояджер-2» зробили понад 50 000 знімків, надавши вченим значну
          інформацію про атмосферу, магнітні поля і геологію найбільшої планети Сонячної системи.</h4><br>
      </div>
      <div>
        <br><b>
          <h3>Сатурн</h3>
        </b><br>
        <h4 class="text-lg; text-end">
          У 1980 та 1981 роках зонди досягли Сатурна, надавши вченим безпрецедентне розуміння кільцевої структури,
          атмосфери та супутників планети.Щоб зробити цю фотографію, NASA використало три знімки «Вояджера-2», зроблені
          через ультрафіолетовий, фіолетовий та зелений фільтри:
        </h4><br>
      </div>
    </CardContent>
  </Card>
</template>

<style>
.cont {
  display: flex;
}

.container1 {
  max-width: 370px;
}

@media (max-width: 750px) {
  .cont {
    display: grid;
  }

  .container1 {
    max-width: 100%;
  }
}

.shadow {
  box-shadow: 5px 5px 50px 0px rgba(198, 198, 198, 0.04);

}
</style>
