<template>
    <footer class="border-t ">
        <div class="mx-48 p-8 px-4 grid grid-cols-12 gap-4">
            <div class=" col-span-4 grid grid-cols-2 gap-4">
                <div class="flex flex-col gap-4">
                    <p><strong>Tokopedia</strong></p>
                    <p v-for="item in tokped" :key="item" class="text-xs opacity-65">{{ item.title }}</p>
                </div>
                <div class="flex flex-col gap-4">
                    <p><strong>Beli</strong></p>
                    <p v-for="item in beli" :key="item" class="text-xs opacity-65">{{ item.title }}</p>
                    <p><strong>Jual</strong></p>
                    <p v-for="item in jual" :key="item" class="text-xs opacity-65">{{ item.title }}</p>
                    <p><strong>Bantuan dan Panduan</strong></p>
                    <p v-for="item in help" :key="item" class="text-xs opacity-65">{{ item.title }}</p>
                </div>
            </div>
            <div class=" col-span-3">x</div>
            <div class=" col-span-5 relative">
                <img src="https://images.tokopedia.net/img/unify/il_footer_hd_v2.png" alt="">
            </div>
        </div>
    </footer>
</template>
<script>
export default {
    data() {
        return {
            tokped: [
                {
                    title: "Tentang Tokopedia"
                },
                {
                    title: "Hak Kekayaan Intelektual"
                },
                {
                    title: "Karir"
                },
                {
                    title: "Blog"
                },
                {
                    title: "Tokopedia Parents"
                },
                {
                    title: "Tokopedia Affiliate Program"
                },
                {
                    title: "Tokopedia B2B Digital"
                },
                {
                    title: "Tokopedia B2B Marketing Solutions"
                },
                {
                    title: "Kalkulator Indeks Masa Tubuh"
                },
                {
                    title: "Tokopedia Farma"
                },
                {
                    title: "Promo Hari Ini"
                },
                {
                    title: "Langsung LAku"
                },
                {
                    title: "Beli Lokal"
                },
                {
                    title: "Tukar Tambah Laptop"
                },
                {
                    title: "Promo 6.6"
                },
            ],
            beli: [
                {
                    title: "Tagihan & Top Up"
                },
                {
                    title: "Tokopedia COD"
                },
                {
                    title: "Bebas Ongkir"
                }
            ],
            jual: [
                {
                    title: "Pusat Edukasi Seller"
                },
                {
                    title: "Daftar Official Store"
                },
            ],
            help: [
                {
                    title: "Tokopedia Care"
                },
                {
                    title: "Syarat dan Ketentuan"
                },
                {
                    title: "Kebijakan Privasi"
                },
            ],
        }
    },
}
</script>