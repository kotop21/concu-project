<script setup lang="ts">
import { onMounted } from 'vue'
import { AlignJustify, Home, Satellite, Github, Rocket, BookOpenText} from 'lucide-vue-next'
import { Button } from '@/components/ui/button'
import {
  DropdownMenu,
  DropdownMenuContent,
  DropdownMenuItem,
  DropdownMenuSeparator,
  DropdownMenuTrigger,
} from '@/components/ui/dropdown-menu'

</script>


<template>
  <header class="fixed-header">
    <div class="header-container">
      <div class="header-section title-section" style="font-family: 'e-UkraineHead-LOGO', sans-serif; font-size: 21px;">
        <p class="shadow">Вояджер</p>
        <Satellite class=""/>
      </div>
      <div class="header-section buttons-section">
        
      </div>
      <div class="header-section theme-switch-section">
        <DropdownMenu>
          <DropdownMenuTrigger>
            <Button variant="outline" size="icon">
              <AlignJustify class="w-4 h-4" />
            </Button>
          </DropdownMenuTrigger>
          <DropdownMenuContent>

              <DropdownMenuItem>
                <Github class="mr-2 h-4 w-4"/>
                <a target="_blank" href="https://github.com/kotop21/concu-project">Github</a>
              </DropdownMenuItem>
              <DropdownMenuSeparator />
            <DropdownMenuItem>
              <Rocket class="mr-2 h-4 w-4"/>
              <a target="_blank" href="https://voyager.jpl.nasa.gov/">Nasa</a>
            </DropdownMenuItem>
            <DropdownMenuItem>
              <BookOpenText class="mr-2 h-4 w-4"/>
              <a target="_blank" href="https://ru.wikipedia.org/wiki/%D0%92%D0%BE%D1%8F%D0%B4%D0%B6%D0%B5%D1%80-1">Wikipedia</a>
            </DropdownMenuItem>
          </DropdownMenuContent>
        </DropdownMenu>
      </div>
    </div>
  </header>
</template>

<style scoped>
.buttons-section {
  width: 87vh;
}

header {
  display: flex;
  justify-content: center;
  height: 60px;
}
.fixed-header {
  position: fixed;
  width: 100%;
  z-index: 2;
  backdrop-filter: blur(10px);
  transition: background-color 0.3s ease; /* Анимация изменения цвета фона */
}

.header-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px; /* Добавлен отступ для красоты */
}

.title-section {
    padding-left: 43px;
}


.header-section {
  display: flex;
  align-items: center;
}

/* Media query for 800px and below */
@media (max-width: 850px) {
  .title-section,
  .theme-switch-section {
    position: fixed;

    padding: 20px;
    z-index: 1001; /* Ensure it's above the .fixed-header */
  }

  .title-section {
    left: 0;
  }

  .theme-switch-section {
    right: 0;
  }
}
</style>
