<template>
    <div class="doc-main">
        <div class="doc-intro">
            <h1>ProgressSpinner Theming</h1>
        </div>
        <DocSections :docs="docs" />
    </div>
    <DocSectionNav :docs="docs" />
</template>

<script>
import DocApiTable from '@/components/doc/DocApiTable.vue';
import DocStyledPreset from '@/components/doc/DocStyledPreset.vue';
import { getStyleOptions, getTokenOptions } from '@/components/doc/helpers';
import TailwindDoc from './TailwindDoc.vue';

export default {
    data() {
        return {
            docs: [
                {
                    id: 'theming.styled',
                    label: 'Styled',
                    children: [
                        {
                            id: 'theming.classes',
                            label: 'CSS Classes',
                            description: 'List of class names used in the styled mode.',
                            component: DocApiTable,
                            data: getStyleOptions('ProgressSpinner')
                        },
                        {
                            id: 'theming.tokens',
                            label: 'Design Tokens',
                            description: 'List of design tokens.',
                            component: DocApiTable,
                            data: getTokenOptions('ProgressSpinner')
                        },
                        {
                            id: 'theming.preset',
                            label: 'Built-in Presets',
                            component: DocStyledPreset,
                            data: 'progressspinner'
                        }
                    ]
                },
                {
                    id: 'theming.unstyled',
                    label: 'Unstyled',
                    description: 'Theming is implemented with the pass through properties in unstyled mode.',
                    children: [
                        {
                            id: 'theming.tailwind',
                            label: 'Tailwind',
                            component: TailwindDoc
                        }
                    ]
                }
            ]
        };
    }
};
</script>
