<template>
    <header class=" flex items-center flex-col">
        <div class="bg-[#F0F3F7] h-7 flex items-center justify-between w-full px-9 text-xs text-[#6F7789]">
            <span class="hover:text-[#00AA5B] cursor-pointer ">Download Tokopedia App</span>
            <div class="flex gap-8">
                <span class=" hover:text-[#00AA5B] cursor-pointer">Tentang Tokopedia</span>
                <span class=" hover:text-[#00AA5B] cursor-pointer">Mitra Tokopedia</span>
                <span class=" hover:text-[#00AA5B] cursor-pointer">Pusat Edukasi Seller</span>
                <span class=" hover:text-[#00AA5B] cursor-pointer">Promo</span>
                <span class=" hover:text-[#00AA5B] cursor-pointer">Tokopedia Care</span>
            </div>
        </div>
        <nav class=" h-16 flex items-center justify-between w-full px-8 gap-9">
            <div class="relative w-[150px]">
                <img src="https://images.tokopedia.net/assets-tokopedia-lite/v2/zeus/production/e5b8438b.svg" alt="logo">
            </div>
            <div class="flex flex-1 items-center gap-5">
                <span>Kategori</span>
                <input type="text" class="border rounded-md w-full p-2">
            </div>
            <div class="flex items-center gap-4">
                <span class="flex relative hover:bg-slate-100 p-1 rounded-lg">
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="size-6">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M2.25 3h1.386c.51 0 .955.343 1.087.835l.383 1.437M7.5 14.25a3 3 0 0 0-3 3h15.75m-12.75-3h11.218c1.121-2.3 2.1-4.684 2.924-7.138a60.114 60.114 0 0 0-16.536-1.84M7.5 14.25 5.106 5.272M6 20.25a.75.75 0 1 1-1.5 0 .75.75 0 0 1 1.5 0Zm12.75 0a.75.75 0 1 1-1.5 0 .75.75 0 0 1 1.5 0Z" />
                    </svg>
                    <span class="absolute right-0 top-0 bg-[#E02954] p-1 text-white rounded-full text-xs h-4 min-w-4 inline-flex items-center justify-center">{{count}}</span>
                </span>
                <span class="flex relative hover:bg-slate-100 p-1 rounded-lg">
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="size-6">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M14.857 17.082a23.848 23.848 0 0 0 5.454-1.31A8.967 8.967 0 0 1 18 9.75V9A6 6 0 0 0 6 9v.75a8.967 8.967 0 0 1-2.312 6.022c1.733.64 3.56 1.085 5.455 1.31m5.714 0a24.255 24.255 0 0 1-5.714 0m5.714 0a3 3 0 1 1-5.714 0" />
                    </svg>
                    <span class="absolute right-0 top-0 bg-[#E02954] p-1 text-white rounded-full text-xs h-4 min-w-4 inline-flex items-center justify-center">{{count}}</span>
                </span>
                <span class="flex relative hover:bg-slate-100 p-1 rounded-lg">
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="size-6">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M21.75 6.75v10.5a2.25 2.25 0 0 1-2.25 2.25h-15a2.25 2.25 0 0 1-2.25-2.25V6.75m19.5 0A2.25 2.25 0 0 0 19.5 4.5h-15a2.25 2.25 0 0 0-2.25 2.25m19.5 0v.243a2.25 2.25 0 0 1-1.07 1.916l-7.5 4.615a2.25 2.25 0 0 1-2.36 0L3.32 8.91a2.25 2.25 0 0 1-1.07-1.916V6.75" />
                    </svg>
                    <span class="absolute right-0 top-0 bg-[#E02954] p-1 text-white rounded-full text-xs h-4 min-w-4 inline-flex items-center justify-center">{{count}}</span>
                </span>
                <div class="border h-7"></div>
                <span class="flex items-center gap-4 hover:bg-slate-100 p-1 rounded-lg">
                    <div class="relative w-8 h-8 aspect-square">
                        <img class="rounded-full" src="https://images.tokopedia.net/img/seller_no_logo_2.png" alt="">
                    </div>
                    <span>toko</span>
                </span>
                <span class="flex items-center gap-4 hover:bg-slate-100 p-1 rounded-lg">
                    <div class="relative w-8 h-8 aspect-square">
                        <img class="rounded-full" src="https://images.tokopedia.net/img/cache/300/tPxBYm/2023/1/20/d377127f-9f8d-4af2-94c4-8246bb4587ca.jpg" alt="">
                    </div>
                    <span>profile</span>
                </span>
            </div>
        </nav>
        <div class="border-b h-7 flex items-center justify-between w-full px-9 text-xs text-[#6F7789]">
            <div class="w-[16vw]" />
            <div class="flex flex-1 gap-4">
                <span v-for="item in 7" :key="item" class=" hover:text-[#00AA5B] cursor-pointer">New Era {{item}}</span>
            </div>
            <div class="flex gap-8">
                <span class=" hover:text-[#00AA5B] cursor-pointer">Dikirim ke <strong>Rumah</strong></span>
            </div>

        </div>
    </header>
</template>

<script>
export default {
    data() {
        return {
            data: null
        }
    },
    props:{
        count:{
            type: Number,
            required: true
        }
    }
}
</script>