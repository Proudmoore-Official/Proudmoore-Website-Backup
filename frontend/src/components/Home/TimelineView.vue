<script setup lang="ts">
import { useI18n } from 'vue-i18n';

const { t } = useI18n();
</script>

<template>
    <section
        id="timeline"
        class="pt-[100px] flex flex-col items-center justify-center [@media(max-width:1450px)]:px-8"
    >
        <!-- Texte + warning visible uniquement <1450px -->
        <div class="block [@media(min-width:1450px)]:hidden text-center">
            <div
            class="mb-10 bg-yellow-100 border-l-4 border-yellow-500 text-yellow-700 p-4 rounded-md shadow-md"
            >
            ⚠️ The full timeline is only available on desktop format (above 1450px)
            </div>
        <h3 class="mb-[1.7rem] font-marcellus timeline-title">
            {{ t('timeline.title') }}
        </h3>
        <p class="font-marcellus timeline-title mb-4">
            {{ t('timeline.description') }}
        </p>
        </div>

        <!-- Image visible uniquement >=1450px -->
        <div class="hidden [@media(min-width:1450px)]:flex w-full overflow-x-auto [@media(min-width:1450px)]:flex-col [@media(min-width:1450px)]:items-center [@media(min-width:1450px)]:justify-center">
            <h3 class="mb-[4rem] font-marcellus timeline-title">
                <!-- {{ t('timeline.mainTitle') }} -->
                Timeline
            </h3>
            <img
                src="/webp/25-timeline.svg"
                alt="Timeline Image"
                class="h-auto w-full"
            />
        </div>
    </section>
</template>
