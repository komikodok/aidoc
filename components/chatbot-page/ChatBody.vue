<script setup lang="ts">
import { motion } from 'motion-v';
import UserMessage from './UserMessage.vue';
import BotMessage from './BotMessage.vue';
import { type IMessage } from '~/types/message.type';

const { messages } = defineProps<{
  messages: IMessage[],
}>();


</script>

<template>
  <motion.div 
    class="absolute bg-gradient-to-b from-cyan-100/90 via-cyan-100/80 to-white overflow-y-auto w-full h-[95%] py-28 px-6"
  >
    <div class="max-w-3xl mx-auto">
      <div v-for="(message, index) in messages">
        <div :key="index">
          <UserMessage 
            v-if="message.role === 'user'" 
            :role="message.role" 
            :content="message.content"
          />
          <BotMessage 
            v-else-if="message.role === 'bot'" 
            :role="message.role" 
            :content="message.content" 
          />
        </div>
      </div>
    </div>
  </motion.div>
</template>

