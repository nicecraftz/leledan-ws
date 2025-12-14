<template>
  <section id="about" class="relative bg-background/90 py-10 px-6 md:py-20">
    <div class="max-w-5xl mx-auto grid grid-cols-1 md:grid-cols-5 gap-10 items-center">
      <!-- Avatar section, visually prioritized on desktop -->
      <div class="md:col-span-2 flex justify-center md:justify-end">
        <div class="relative group">
          <img
            src="/images/profile_picture.webp"
            alt="Minecraft avatar"
            class="w-48 h-48 md:w-72 md:h-72 object-cover rounded-3xl border-4 border-primary shadow-2xl shadow-primary/30 bg-background transition-transform duration-300 group-hover:scale-105"
          />
          <!-- Fancy ring effect behind avatar -->
          <span class="absolute inset-0 rounded-3xl ring-4 ring-primary/30 animate-pulse -z-10"></span>
        </div>
      </div>
      <!-- Bio text section -->
      <div class="md:col-span-3 flex flex-col items-start">
        <h1 class="text-3xl md:text-4xl font-extrabold text-primary tracking-wide mb-4">
          Chi sono
        </h1>
        <div class="space-y-5 text-text text-lg leading-relaxed tracking-wide">
          <p>
            <span class="font-semibold text-primary">Heyla!</span> Sono lele, un costruttore professionista di Minecraft specializzato in
            <span class="text-primary font-semibold">creazioni organiche</span>, 
            <span class="text-primary font-semibold">terraforming avanzato</span> 
            e <span class="text-primary font-semibold">strutture epiche</span>.
          </p>
          <p>
            Con anni di esperienza, creo mondi immersivi che fondono 
            <span class="text-primary font-semibold">realismo naturale</span> 
            e <span class="text-primary font-semibold">design architettonico</span>.
            Sul mio 
            <a href="https://www.youtube.com/@leledan06" target="_blank" rel="noopener" class="underline decoration-primary hover:text-primary font-semibold transition-colors">canale YouTube</a>
            condivido sia video di building dettagliati che avventure coinvolgenti, portando la community dentro il mio processo creativo.
          </p>
          <div class="grid grid-cols-2 gap-3">
            <ul class="space-y-1 list-none marker:text-primary">
              <li>
                <UIcon name="i-lucide-flower" class="inline-block mr-2 text-primary" /> <span>Foreste lussureggianti</span>
              </li>
              <li>
                <UIcon name="i-lucide-mountain" class="inline-block mr-2 text-primary" /> <span>Montagne mozzafiato</span>
              </li>
            </ul>
            <ul class="space-y-1 list-none marker:text-primary">
              <li>
                <UIcon name="i-lucide-building-2" class="inline-block mr-2 text-primary" /> <span>Città medievali</span>
              </li>
              <li>
                <UIcon name="i-lucide-stars" class="inline-block mr-2 text-primary" /> <span>Strutture fantasy</span>
              </li>
            </ul>
          </div>
          <p>Da idee a <span class="text-primary font-bold">Sculture Professionali</span>.</p>
          <p>
            <span class="font-semibold">La mia missione</span> è ispirare e aiutare altre persone a specializzarsi in questo campo, mostrando le infinite possibilità creative di Minecraft.
          </p>
        </div>
      </div>
    </div>
  </section>
</template>