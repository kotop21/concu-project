<script setup lang="ts">
import { ChevronRight } from 'lucide-vue-next'
import { Button } from '@/components/ui/button'

</script>

<template>
    <header>
      <div class="header-container">
        <div class="header-section title-section" style="font-family: 'e-UkraineHead-LOGO', sans-serif; font-size: 20px;">
          <p>Вояджер</p>
        </div>
        <div class="header-section buttons-section">
          <!-- Add your buttons here -->
            <Button variant="ghost">Головна</Button>
            <Button variant="ghost">Історія</Button>
          <!-- Add more buttons as needed -->
        </div>
        <div class="header-section theme-switch-section">
            <Button variant="outline" size="icon"><Mail class="w-4 h-4 mr-2" /></Button>
          <!-- Add your theme switch element here -->
        </div>
      </div>
    </header>
  </template>
  
  <style scoped>
  header {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 56px;
    backdrop-filter: blur(10px);
    z-index: 1000;
  }
  
  .header-container {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    width: 80%; /* Adjust as needed */
    margin: 10px auto 0; /* Center the header with top margin */
  }
  
  .header-section {
    flex: 1;
    text-align: center;
  }
  
  .title-section {
    /* Styles for the title section */
  }
  
  .buttons-section {
    /* Styles for the buttons section */
  }
  
  .theme-switch-section {
    /* Styles for the theme switch section */
  }
  </style>
  
  