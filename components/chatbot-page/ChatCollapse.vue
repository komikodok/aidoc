<script setup lang="ts">
const emit = defineEmits<{
  (e: 'select-collapse', name: string): void;
}>();

const handleClick = (event: MouseEvent) => {
  const target = event.target as HTMLElement;
  emit('select-collapse', target.innerText.trim());
  navigateTo(`/konsultasi/${target.innerText.trim().toLowerCase()}`)
};
</script>

<template>
    <ul class="w-full h-full flex flex-col gap-4 p-4">
        <!-- Specialist 1 -->
        <li class="collapse collapse-arrow rounded-xl shadow-md ">
            <input type="checkbox" class="peer" />
            <div
                class="collapse-title bg-base-100 font-semibold   text-neutral peer-checked:bg-sky-300 rounded-t-2xl"
            >
                🩺 Poli Dalam
            </div>
            <ul
                class="collapse-content flex flex-col gap-2 bg-base-100 text-neutral peer-checked:text-neutral"
            >
                <li @click="handleClick" class="p-1 cursor-pointer hover:bg-gray-100 active:bg-gray-100  ">Diabetes</li>
                <li @click="handleClick" class="p-1 cursor-pointer hover:bg-gray-100 active:bg-gray-100  ">Darah Tinggi</li>
                <li @click="handleClick" class="p-1 cursor-pointer hover:bg-gray-100 active:bg-gray-100  ">Kolesterol</li>
            </ul>
        </li>

        <!-- Specialist 2 -->
        <li class="collapse collapse-arrow rounded-xl shadow-md ">
            <input type="checkbox" class="peer" />
            <div
                class="collapse-title bg-base-100 font-semibold   text-neutral peer-checked:bg-sky-300 rounded-t-2xl"
            >
                🩺 Poli Jantung
            </div>
            <ul
                class="collapse-content flex flex-col gap-2 bg-base-100 text-neutral peer-checked:text-neutral"
            >
                <li @click="handleClick" class="p-1 cursor-pointer hover:bg-gray-100 active:bg-gray-100">Penyakit Jantung</li>
            </ul>
        </li>

        <!-- Specialist 3 -->
        <li class="collapse collapse-arrow rounded-xl shadow-md ">
            <input type="checkbox" class="peer" />
            <div
                class="collapse-title bg-base-100 font-semibold   text-neutral peer-checked:bg-sky-300 rounded-t-2xl"
            >
                🩺 Poli Paru
            </div>
            <ul
                class="collapse-content flex flex-col gap-2 bg-base-100 text-neutral peer-checked:text-neutral"
            >
                <li @click="handleClick" class="p-1 cursor-pointer hover:bg-gray-100 active:bg-gray-100  ">Penyakit Paru-paru</li>
            </ul>
        </li>

        <!-- Specialist 4 -->
        <li class="collapse collapse-arrow rounded-xl shadow-md ">
            <input type="checkbox" class="peer" />
            <div
                class="collapse-title bg-base-100 font-semibold   text-neutral peer-checked:bg-sky-300 rounded-t-2xl"
            >
                🩺 Poli Kulit
            </div>
            <ul
                class="collapse-content flex flex-col gap-2 bg-base-100 text-neutral peer-checked:text-neutral"
            >
                <li @click="handleClick" class="p-1 cursor-pointer hover:bg-gray-100 active:bg-gray-100  ">Penyakit Kulit</li>
            </ul>
        </li>

        <!-- Specialist 5 -->
        <li class="collapse collapse-arrow rounded-xl shadow-md ">
            <input type="checkbox" class="peer" />
            <div
                class="collapse-title bg-base-100 font-semibold   text-neutral peer-checked:bg-sky-300 rounded-t-2xl"
            >
                🩺 Poli Onkologi
            </div>
            <ul
                class="collapse-content flex flex-col gap-2 bg-base-100 text-neutral peer-checked:text-neutral"
            >
                <li @click="handleClick" class="p-1 cursor-pointer hover:bg-gray-100 active:bg-gray-100  ">Kanker</li>
            </ul>
        </li>
       
    </ul>
</template>