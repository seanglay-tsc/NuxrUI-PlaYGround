<script setup lang="ts">
import { CalendarDate } from '@internationalized/date'

const calendarValue = shallowRef(new CalendarDate(2025, 1, 10))

const placeholder = shallowRef(calendarValue.value)
const minValue = shallowRef(new CalendarDate(1999, 3, 15))
const maxValue = shallowRef(new CalendarDate(2030, 3, 15))
</script>

<template>
  <UApp>
    <div class="flex flex-col items-center justify-center h-screen">
      <UCalendar v-model="calendarValue" v-model:placeholder="placeholder" :min-value="minValue" :max-value="maxValue">
        <template #heading="{ value }">
          <CalendarYearMonthSelect v-model:placeholder="placeholder" :min-value="minValue" :max-value="maxValue">
            {{ value }}
          </CalendarYearMonthSelect>
        </template>
      </UCalendar>
    </div>
  </UApp>
</template>
