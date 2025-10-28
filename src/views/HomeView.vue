<script setup>
import { useHead } from '@unhead/vue'
import AppSidebar from '@/components/AppSidebar.vue'
import AppHeader from '@/components/AppHeader.vue'
import AppFooter from '@/components/AppFooter.vue'

import AppPromo from '@/components/AppPromo.vue'
import AppDestinations from '@/components/AppDestinations.vue'
import AppActivities from '@/components/AppActivities.vue'
import AppPriceCalendar from '@/components/AppPriceCalendar.vue'

useHead({ title: 'Twoja przygoda już na Ciebie czeka' })
</script>

<template>
  <div class="min-h-screen flex">
    <AppSidebar />
    <AppHeader />

    <div class="flex-1 flex flex-col lg:pl-64">
      <main class="flex-grow">
        <!-- Promo section -->
        <AppPromo
          imageUrl="/images/home-promo.png"
          title="Rozpocznij swoją kolejną przygodę!"
          subtitle="Porównuj i odkrywaj najciekawsze oferty lotów i podróży dzięki naszej wygodnej, intuicyjnej platformie."
        />

        <!-- Country section -->
        <AppDestinations :isBtnShow="true" :countOfCountries="3" />

        <!-- Price Calendar -->
        <AppPriceCalendar />

        <!-- Services -->
        <AppActivities
          title="Najpopularniejsze atrakcje"
          subtitle="Odkrywaj niezwykłe doświadczenia i ekscytujące aktywności, które dodadzą Twojej podróży niezapomnianych emocji i wyjątkowego charakteru."
        />
      </main>

      <AppFooter />
    </div>
  </div>
</template>
