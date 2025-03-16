# Cannot find name 'useNuxtDevTools'

According to https://devtools.nuxt.com/guide/composables you can use the `useNuxtDevTools` composable which is auto-imported. But I am getting an error that it is not found:

> Cannot find name 'useNuxtDevTools'.ts-plugin (2304)

This seems to be only a type bug because in runtime it works.

```vue
<script setup lang="ts">
    const devtoolsClient = useNuxtDevTools() // Cannot find name 'useNuxtDevTools'.ts-plugin(2304)

    const openDevtools = () => {
        devtoolsClient.value.devtools.toggle() // This works!
    }
</script>
```
