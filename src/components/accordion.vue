<template>
  <div class="flex sm:w-[590px] md:w-[850px] xl:w-[850px]">
    <div class="xl:p-[50px_0] xl:text-base xl:leading-[1.4em] w-full">
      <div class="accordion">
        <div class="arrcordion__wrapper">
          <div
            class="accordion__group"
            v-for="(item, index) in accordion"
            :key="index"
          >
            <div
              @click="handleActive(item.id)"
              class="cursor-pointer gap-4 p-[20px_0] sm:flex sm:justify-between sm:items-center xl:flex xl:justify-between xl:items-center"
            >
              <button
                aria-label="number of faq studio noice"
                :class="
                  isActive === item.id
                    ? 'bg-[#fad810] text-black'
                    : 'bg-[#454545]'
                "
                href="#_"
                class="inline-flex items-center rounded-md justify-center sm:py-1 sm:px-2 xl:px-3.5 xl:py-[10px] text-base font-medium"
              >
                0{{ item.id }}
              </button>
              <div
                :class="isActive === item.id ? 'font-bold' : 'font-normal'"
                class="lg:text-xl text-[#d6d6d6] select-none w-full"
              >
                {{ item.title }}
              </div>
              <svg
                data-accordion-icon
                :class="isActive === item.id ? '-rotate-90' : ''"
                class="w-6 h-6 shrink-0"
                :fill="isActive === item.id ? '#fad810' : 'currentColor'"
                viewBox="0 0 20 20"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  fill-rule="evenodd"
                  d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z"
                  clip-rule="evenodd"
                ></path>
              </svg>
            </div>
            <transition name="slide">
              <div
                class="accordion__content"
                v-show="isActive === item.id"
                ref="item"
              >
                <div class="xl:p-[20px_0]">
                  <p
                    :class="
                      index !== 0
                        ? 'sm:text-base xl:text-lg'
                        : 'text-base font-bold'
                    "
                    v-for="(data, index) in item.content"
                    :key="index"
                  >
                    <span>{{ data }}</span>
                  </p>
                </div>
              </div>
            </transition>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Accordion",
  data() {
    return {
      accordion: [
        {
          id: 1,
          title: "Bagaimana cara mendaftarkan podcast ke Noice?",
          content: [
            "Cara mendaftarkan podcast di Noice",
            "Kunjungi website studio.noice.id, masuk ke akun Noicemu",
            "Klik tombol “Tambah Podcast” lalu pilih “Masukin Link RSS” dan ikuti semua tahapan yang ada",
            "Pastikan podcastmu sudah sesuai dengan “Ketentuan Konten yang Berlaku”",
          ],
        },
        {
          id: 2,
          title:
            "Bagaimana cara menghubungkan akun Noice saya ke podcast yang ada di Noice?",
          content: [
            "Cara menghubungkan podcast di Noice ke akun",
            "Kunjungi website studio.noice.id lalu masuk ke akun Noicemu",
            "Klik tombol “Tambah Podcast",
            "Pilih “Tampilkan Podcast” dan lanjutkan semua tahapan",
          ],
        },
        {
          id: 3,
          title: "Kenapa tidak ada email verifikasi yang diterima?",
          content: [
            "Pastikan kamu mengirim verifikasi ke email yang terhubung dengan RSS feed podcastmu, jika belum menerima coba refresh halaman kotak masuk atau cek kotak spam.Kamu juga bisa mendapatkan tautan verifikasi baru dengan cara klik “Kirim Ulang”",
          ],
        },
        {
          id: 4,
          title: "Apakah data di dashboard up to date?",
          content: [
            "Tentu saja, data pada dashboard diperbarui setiap hari, namun perlu dipahami bahwa Noice perlu waktu untuk menampilkan data ke dashboard. Jadi, cek secara berulang ya.",
          ],
        },
      ],
      isActive: null,
    };
  },
  methods: {
    handleActive(id) {
      if (this.isActive === id) {
        this.isActive = null;
      } else {
        this.isActive = id;
      }
    },
    filterArray(string) {
      return string === "studio.noice.id";
    },
  },
};
</script>
