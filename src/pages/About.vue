<template>
  <PageWrapper class="flex flex-col justify-center" id="about" v-bind="props">
    <Header>ABOUT</Header>


    <div class="flex flex-col gap-8 pl-4 2xl:w-[90%] 2xl:flex-row 2xl:gap-60 2xl:pl-8 [&>*]:flex-1">
      <div class="flex flex-col gap-8">
        <div>
          <p>Quantum physics researcher & AI systems engineer.</p>
          <p>Building bridges between quantum computing, machine learning, and cybersecurity.</p>
        </div>


        <div class="hidden gap-2 text-secondary 2xl:flex">
          <img src="/icons/python.svg" alt="python" />
          <span>Python is my lingua franca</span>
        </div>
      </div>


      <p class="mb-8 2xl:mb-0">
        I'm a physicist with specialized expertise in quantum many-body systems 
        and neural quantum states. My journey spans from theoretical quantum phase transitions in 
        optical cavities to practical quantum machine learning on near-term processors.
        <br />
        I learn by building. Every project—thesis research, SDK development, agentic RAG/AI systems 
        teaches me something about constraints, scalability, and what it means to move from theory 
        to production. I stay current by reading papers critically, experimenting with new frameworks, 
        and collaborating with researchers and engineers who push boundaries.
      </p>
    </div>
    <div class="ml-4 flex gap-2 text-secondary 2xl:hidden">
      <img src="/icons/python.svg" alt="python" />
      <span>Python is my lingua franca</span>
    </div>


    <CloseBracket />
  </PageWrapper>
</template>


<script setup lang="ts">
import Header from "@/components/Header.vue";
import PageWrapper from "@/components/PageWrapper.vue";
import CloseBracket from "@/components/CloseBracket.vue";
import type { PageProps } from "@/utils/pages";


const props = defineProps<PageProps>();
</script>
