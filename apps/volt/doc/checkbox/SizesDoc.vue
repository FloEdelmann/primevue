<template>
    <DocSectionText v-bind="$attrs">
        <p>Checkbox provides <i>small</i> and <i>large</i> sizes as alternatives to the base.</p>
    </DocSectionText>
    <div class="card flex flex-wrap justify-center gap-4">
        <div class="flex items-center gap-2">
            <Checkbox v-model="size" inputId="size_small" name="size" value="Small" size="small" />
            <label for="size_small" class="text-sm">Small</label>
        </div>
        <div class="flex items-center gap-2">
            <Checkbox v-model="size" inputId="size_normal" name="size" value="Normal" />
            <label for="size_normal">Normal</label>
        </div>
        <div class="flex items-center gap-2">
            <Checkbox v-model="size" inputId="size_large" name="size" value="Large" size="large" />
            <label for="size_large" class="text-lg">Large</label>
        </div>
    </div>
    <DocSectionCode :code="code" />
</template>

<script setup lang="ts">
import Checkbox from '@/volt/Checkbox.vue';
import { ref } from 'vue';

const size = ref(null);

const code = ref(`
<template>
    <div class="card flex flex-wrap justify-center gap-4">
        <div class="flex items-center gap-2">
            <Checkbox v-model="size" inputId="size_small" name="size" value="Small" size="small" />
            <label for="size_small" class="text-sm">Small</label>
        </div>
        <div class="flex items-center gap-2">
            <Checkbox v-model="size" inputId="size_normal" name="size" value="Normal" />
            <label for="size_normal">Normal</label>
        </div>
        <div class="flex items-center gap-2">
            <Checkbox v-model="size" inputId="size_large" name="size" value="Large" size="large" />
            <label for="size_large" class="text-lg">Large</label>
        </div>
    </div>
</template>

<script setup lang="ts">
import Checkbox from '@/volt/Checkbox.vue';
import { ref } from 'vue';

const size = ref(null);
<\/script>
`);
</script>
