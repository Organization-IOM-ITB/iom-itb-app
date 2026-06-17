<template>
  <div class="max-w-[1400px] mx-auto">
    <h2 class="text-main font-[800] text-[32px] md:text-[50px] text-center leading-tight md:leading-[65.1px] py-[16px]">Grafik</h2>
    <div class="flex flex-col md:flex-row justify-between md:items-center mb-[8px] gap-2 md:px-10">
      <div class="flex gap-2 items-center">
        <button @click="modeHandler('report')" :class="`${mode === 'report' ? 'text-white bg-main' : 'text-main bg-white'} border border-main px-[8px] py-[4px] w-fit h-fit rounded-[5px] text-[14px] md:text-[16px] text-center font-bold tracking-tight`">Laporan</button>
        <button @click="modeHandler('year')" :class="`${mode === 'year' ? 'text-white bg-main' : 'text-main bg-white'} border border-main px-[8px] py-[4px] w-fit h-fit rounded-[5px] text-[14px] md:text-[16px] text-center font-bold tracking-tight`">Pertahun</button> 
        <button @click="modeHandler('grade')" :class="`${mode === 'grade' ? 'text-white bg-main' : 'text-main bg-white'} border border-main px-[8px] py-[4px] w-fit h-fit rounded-[5px] text-[14px] md:text-[16px] text-center font-bold tracking-tight`">Perangkatan</button>
      </div>
      <div class="w-full md:w-fit h-fit flex">
        <select id="countries" class="bg-gray-50 border border-gray-300 text-gray-900 text-[14px] md:text-[16px] rounded-[5px] focus:ring-blue-500 focus:border-blue-500 block w-full px-[8px] py-[4px]" v-model="graphic">
          <option v-for="(opt, index) in options" :key="index" :value="index">{{ opt }}</option>
        </select>
      </div>
    </div>
    <div class="bg-white rounded-2xl shadow-sm border border-gray-100 mt-4 overflow-hidden">
      <img :src="currentImages[graphic] || currentImages[0]" class="w-full md:px-10 md:py-8 object-contain" />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      data: [
        {
          category: 'report', 
          options: ['Rekap Penyaluran', 'Jumlah Penerima'],
          graphic: [
            require('@/assets/image/penyaluran-bantuan-iom-itb.png'),
            require('@/assets/image/jumlah-penerima-bantuan-iom-itb.png')
          ]
        },
        {
          category: 'year', 
          options: ['Rekap Semua', 'Biaya Hidup', 'Tugas Akhir', 'UKT'],
          graphic: [
            require('@/assets/image/grafik-penerimaan-bantuan-iom-2025.png'),
            require('@/assets/image/grafik-rekap-pertahun.png'),
            require('@/assets/image/grafik-biaya-hidup-pertahun.png'),
            require('@/assets/image/grafik-tugas-akhir-pertahun.png'),
            require('@/assets/image/grafik-ukt-pertahun.png')
          ]
        },
        {
          category: 'grade', 
          options: ['Rekap Semua', 'Biaya Hidup', 'Tugas Akhir', 'UKT'],
          graphic: [
            require('@/assets/image/grafik-rekap-perangkatan.png'),
            require('@/assets/image/grafik-biaya-hidup-perangkatan.png'),
            require('@/assets/image/grafik-tugas-akhir-perangkatan.png'),
            require('@/assets/image/grafik-ukt-perangkatan.png')
          ]
        }
      ],
      graphic: 0,
      mode: 'report'
    };
  },
  computed: {
    currentCategory() {
      return this.data.find(d => d.category === this.mode);
    },
    options() {
      return this.currentCategory ? this.currentCategory.options : [];
    },
    currentImages() {
      return this.currentCategory ? this.currentCategory.graphic : [];
    }
  },
  methods: {
    modeHandler(v) {
      this.mode = v;
      this.graphic = 0; // Reset select when mode changes
    }
  }
};
</script>
  

  