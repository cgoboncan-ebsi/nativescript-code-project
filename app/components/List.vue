<template>
  <StackLayout height="100%">
    <Label :text="title" fontSize="30" margin="10" />
      <ListView for="i in items" height="100%" separatorColor="transparent" @itemTap="onTap">
        <v-template>
          <StackLayout borderBottomWidth="1" borderBottomColor="#ddd" padding="15">
            <Label :text="i" />
          </StackLayout>
        </v-template>
      </ListView>
  </StackLayout>
</template>

<script lang="ts">
import Vue from 'nativescript-vue'
import { PropType } from 'vue'

/*----- Utils -------*/
type toLabel = (x: number) => string
const toLabel: toLabel = (x) => `Item ${x}`

type range = (start: number, end: number) => number[]
const range: range = (start, end) => Array.from({ length: end - start + 1 }, (_, i) => i)

/*----- Types -------*/
type Props = {
  index: PropType<number>
}

type Data = {
  items: string[]
}

/*----- Component -------*/
export default Vue.extend({
  props: {
    index: Number 
  } as Props,

  computed: {
    title(): string {
      return `List View ${this.index}`
    },
  },

  data(): Data {
    return { items: range(1, 20).map(toLabel) }
  },
  
  methods: {
    onTap(): void {
      console.log('Determine the root cause of why this event handler is not firing.')
    }
  },
})
</script>
