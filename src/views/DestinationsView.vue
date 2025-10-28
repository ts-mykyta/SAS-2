<script setup>
import { useHead } from '@unhead/vue'
import AppSidebar from '@/components/AppSidebar.vue'
import AppHeader from '@/components/AppHeader.vue'
import AppPromo from '@/components/AppPromo.vue'
import AppDestinations from '@/components/AppDestinations.vue'
import AppFooter from '@/components/AppFooter.vue'

useHead({ title: 'Wyrusz tam, gdzie rodzi się prawdziwa przygoda' });

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
          title="Podróż bez granic – odkrywaj miejsca, których nie zapomnisz"
          subtitle="Wyrusz w niezwykłą podróż po zakątkach świata. Od słonecznych plaż po miasta pełne historii – znajdź przestrzeń, w której poczujesz prawdziwą wolność."
        />

        <!-- Country section -->
        <AppDestinations :isBtnShow="false" :countOfCountries="20" />
      </main>

      <AppFooter />
    </div>
  </div>
</template>
