<template>
  <PageWrapper class="flex flex-col justify-center" id="skills" v-bind="props">
    <Header>SKILLS</Header>

    <div class="flex flex-col gap-8 pl-4 2xl:w-[90%] 2xl:flex-row 2xl:gap-60 2xl:pl-8">
      <p>
        I solve problems at the intersection of quantum systems and machine learning by combining theoretical rigor with engineering pragmatism. 
        I build systems that work on constrained hardware, not just in theory. 
        I'm motivated by understanding why things work, then making them work better, doesn't matter if it's physics or code.
      </p>

      <div class="flex justify-between 2xl:gap-40">
        <div class="flex flex-col justify-center gap-3 2xl:gap-6">
          <Skill :skill="language" v-for="language in LANGUAGES" :key="language.name" />
        </div>
        <div class="relative">
          <hr class="absolute h-full w-px bg-secondary 2xl:-top-[20%] 2xl:h-[140%] 2xl:w-1" />
          <hr
            class="absolute h-full w-1 bg-secondary blur-[10px] 2xl:-top-[20%] 2xl:h-[140%] 2xl:w-3 2xl:blur-[20px]"
          />
        </div>
        <div class="flex flex-col justify-center gap-3 2xl:gap-6">
          <Skill :skill="technology" v-for="technology in TECHNOLOGIES" :key="technology.name" />
        </div>
      </div>
    </div>

    <CloseBracket />
  </PageWrapper>
</template>

<script setup lang="ts">
import Header from "@/components/Header.vue";
import Skill from "@/components/Skill.vue";
import PageWrapper from "@/components/PageWrapper.vue";
import CloseBracket from "@/components/CloseBracket.vue";
import type { PageProps } from "@/utils/pages";

const props = defineProps<PageProps>();

const LANGUAGES = [
  {
    name: "Python",
    icon: "python"
  },
  {
    name: "Julia",
    icon: "julia"
  },
  {
    name: "Dart",
    icon: "dart"
  },
  {
    name: "Rust",
    icon: "rust"
  },
  {
    name: "C",
    icon: "c"
  }
];

const TECHNOLOGIES = [
  {
    name: "QuTip",
    icon: "qutip"
  },
  {
    name: "Qiskit",
    icon: "qiskit"
  },
  {
    name: "Pennylane",
    icon: "pennylane"
  },
  {
    name: "QAptiva",
    icon: "qaptiva"
  },
  {
    name: "RAG",
    icon: "rag"
  }
];
</script>
