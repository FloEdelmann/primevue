<template>
    <DocSectionText v-bind="$attrs">
        <p>
            Listbox allows choosing a single item by default, enable <i>multiple</i> property to choose more than one. When the optional <i>metaKeySelection</i> is present, behavior is changed in a way that selecting a new item requires meta key to
            be present.
        </p>
    </DocSectionText>
    <div class="card flex justify-center">
        <Listbox v-model="selectedCity" :options="cities" multiple optionLabel="name" class="w-full md:w-56" />
    </div>
    <DocSectionCode :code="code" />
</template>

<script setup lang="ts">
import Listbox from '@/volt/Listbox.vue';
import { ref } from 'vue';

const selectedCity = ref(null);
const cities = ref([
    { name: 'New York', code: 'NY' },
    { name: 'Rome', code: 'RM' },
    { name: 'London', code: 'LDN' },
    { name: 'Istanbul', code: 'IST' },
    { name: 'Paris', code: 'PRS' }
]);

const code = ref(`
<template>
    <div class="card flex justify-center">
        <Listbox v-model="selectedCity" :options="cities" multiple optionLabel="name" class="w-full md:w-56" />
    </div>
</template>

<script setup lang="ts">
import Listbox from '@/volt/Listbox.vue';
import { ref } from 'vue';

const selectedCity = ref(null);
const cities = ref([
    { name: 'New York', code: 'NY' },
    { name: 'Rome', code: 'RM' },
    { name: 'London', code: 'LDN' },
    { name: 'Istanbul', code: 'IST' },
    { name: 'Paris', code: 'PRS' }
]);
<\/script>
`);
</script>
