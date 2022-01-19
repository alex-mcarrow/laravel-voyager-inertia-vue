<template>
    <div class="min-h-screen flex flex-col sm:justify-center items-center pt-6 sm:pt-0 bg-gray-100">
        <div>
            <Link href="/">
                <BreezeApplicationLogo class="w-20 h-20 fill-current text-gray-500" />
            </Link>
        </div>

        <div class="w-full sm:max-w-md mt-6 px-6 py-4 bg-white shadow-md overflow-hidden sm:rounded-lg">
            <slot />
        </div>
    </div>
</template>

<script>
import BreezeApplicationLogo from '@/Components/ApplicationLogo.vue'
import { Link } from '@inertiajs/inertia-vue3';
import { useToast } from "vue-toastification";

export default {
    components: {
        BreezeApplicationLogo,
        Link,
        useToast
    },
    data() {
        const toast = useToast()
        toast.success("Зырь чо покажу - это тост! За молодожёнов!", {
            timeout: 5000,
        })
        return {
            toast
        }
    }
}
</script>
