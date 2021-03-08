<template>
    <div class="my-card q-pa-xs" :loading='true'>
        <q-img  :src="data.imagePath"  :ratio="16/9" />
        <q-card-section>
            <div class="text-body1">{{ data.title }}</div>
        </q-card-section>
    </div>
</template>

<script>

export default {
  props: {
    data: Object
  }
}
</script>
