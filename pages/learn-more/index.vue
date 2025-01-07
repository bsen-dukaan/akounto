<template>
  <div class="min-h-screen">
    <!-- Navigation -->
    <nav class="bg-neutral-900 text-white fixed w-full z-50">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="flex justify-between h-16 items-center">
          <!-- Logo -->
          <div class="flex-shrink-0 flex items-center">
            <img
              class="h-8 w-auto"
              src="https://dms.mydukaan.io/original/webp/media/dd3b40b1-db23-400d-ae38-bb702bad6fc4.svg"
              alt="Logo"
            />
          </div>

          <!-- Desktop Navigation -->
          <div class="hidden md:block">
            <div class="ml-10 flex items-center space-x-8">
              <a
                href="#"
                v-for="item in menuItems"
                :key="item.text"
                class="text-white hover:text-gray-300"
                >{{ item.text }}</a
              >
              <a
                href="#"
                class="bg-blue-600 hover:bg-blue-700 px-4 py-2 rounded-lg text-sm font-medium text-white"
              >
                Get Started
              </a>
            </div>
          </div>

          <!-- Mobile menu button -->
          <div class="md:hidden">
            <button
              @click="isMobileMenuOpen = !isMobileMenuOpen"
              class="inline-flex items-center justify-center p-2 rounded-md hover:bg-neutral-800"
            >
              <svg
                class="h-6 w-6 text-white"
                stroke="currentColor"
                fill="none"
                viewBox="0 0 24 24"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M4 6h16M4 12h16M4 18h16"
                />
              </svg>
            </button>
          </div>
        </div>

        <!-- Mobile menu -->
        <div v-show="isMobileMenuOpen" class="md:hidden">
          <div class="px-2 pt-2 pb-3 space-y-1">
            <a
              href="#"
              v-for="item in menuItems"
              :key="item.text"
              class="block px-3 py-2 text-base font-medium text-white hover:bg-neutral-800"
            >
              {{ item.text }}
            </a>
            <a
              href="#"
              class="block px-3 py-2 text-base font-medium bg-blue-600 hover:bg-blue-700 rounded-lg text-white"
            >
              Get Started
            </a>
          </div>
        </div>
      </div>
    </nav>

    <!-- Hero Section -->
    <section class="bg-neutral-900 text-white pt-24 pb-16 min-h-[70vh]">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
          <!-- Left Column: Content -->
          <div class="animate__animated animate__fadeInLeft">
            <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold mb-6">
              <span class="text-blue-400">Connect Quickbooks</span> and Akounto
            </h1>
            <p class="text-lg md:text-xl text-gray-300 mb-8">
              Streamline your accounting workflow with automated document
              processing, real-time tracking, and intelligent financial
              insights.
            </p>

            <div class="mt-8 flex items-center gap-4">
              <div class="flex -space-x-2">
                <img
                  v-for="n in 3"
                  :key="n"
                  class="w-10 h-10 rounded-full border-2 border-neutral-900"
                  src="https://www.tradifyhq.com/hubfs/Logo_Plaster-crisp.svg"
                  alt="User"
                />
              </div>
              <p class="text-gray-300">
                Trusted by 10,000+ businesses worldwide
              </p>
            </div>
          </div>

          <!-- Right Column: Image -->
          <div class="relative animate__animated animate__fadeInRight">
            <div class="relative z-10">
              <img
                src="https://www.tradifyhq.com/hs-fs/hubfs/Global%20Hero%20Frame%20extended.webp"
                alt="Dashboard Preview"
                class="w-full rounded-xl shadow-2xl"
              />
            </div>
            <div
              class="absolute inset-0 bg-blue-500/20 blur-3xl -z-10 rounded-full"
            ></div>
          </div>
        </div>

        <!-- Stats Bar -->
        <div
          class="mt-16 grid grid-cols-2 md:grid-cols-4 gap-8 border-t border-neutral-700 pt-8"
        >
          <div v-for="(stat, index) in stats" :key="index" class="text-center">
            <h4 class="text-3xl font-bold text-blue-400">{{ stat.value }}</h4>
            <p class="text-gray-400">{{ stat.label }}</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Features Section -->
    <section class="py-20 bg-white">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-16">
          <h2 class="text-3xl md:text-4xl font-bold text-neutral-900 mb-4">
            Powerful Features for Your Financial Success
          </h2>
          <p class="text-lg text-neutral-600 max-w-2xl mx-auto">
            Streamline your financial operations with our comprehensive suite of
            tools
          </p>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
          <div
            v-for="(feature, index) in features"
            :key="index"
            class="bg-neutral-50 p-6 rounded-xl hover:shadow-xl transition-all duration-300"
          >
            <div
              class="w-14 h-14 bg-blue-100 rounded-lg flex items-center justify-center mb-6"
            >
              <component :is="feature.icon" class="w-8 h-8 text-blue-600" />
            </div>
            <h3 class="text-xl font-bold text-neutral-900 mb-4">
              {{ feature.title }}
            </h3>
            <p class="text-neutral-600">{{ feature.description }}</p>
          </div>
        </div>
      </div>
    </section>

    <!-- CTA Section -->
    <section class="bg-neutral-900 text-white py-20">
      <div class="max-w-7xl mx-auto px-4 text-center">
        <h2 class="text-3xl md:text-4xl font-bold mb-4">
          Ready to get started?
        </h2>
        <p class="text-lg text-gray-300 mb-8">
          Join thousands of businesses already using our platform
        </p>
        <button
          class="bg-blue-600 hover:bg-blue-700 px-8 py-4 rounded-lg text-lg"
        >
          Start Free Trial
        </button>
      </div>
    </section>

    <!-- Footer -->
    <footer class="bg-neutral-900 text-white py-12">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="grid md:grid-cols-4 gap-8">
          <div class="col-span-2">
            <img
              class="h-8 mb-4"
              src="https://dms.mydukaan.io/original/webp/media/dd3b40b1-db23-400d-ae38-bb702bad6fc4.svg"
              alt="Logo"
            />
            <p class="text-gray-400">
              Streamline your financial operations with our comprehensive
              management platform.
            </p>
          </div>
          <div v-for="(section, index) in footerSections" :key="index">
            <h3 class="text-lg font-semibold mb-4">{{ section.title }}</h3>
            <ul class="space-y-2">
              <li v-for="link in section.links" :key="link">
                <a href="#" class="text-gray-400 hover:text-white">{{
                  link
                }}</a>
              </li>
            </ul>
          </div>
        </div>
        <div
          class="border-t border-gray-800 mt-8 pt-8 text-center text-gray-400"
        >
          <p>© {{ new Date().getFullYear() }} Akounto. All rights reserved.</p>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
definePageMeta({
  layout: "blank",
});

export default {
  name: "LearnMore",
  data() {
    return {
      isMobileMenuOpen: false,
      menuItems: [
        { text: "Features" },
        { text: "Pricing" },
        { text: "Resources" },
      ],
      stats: [
        { value: "98%", label: "Processing Accuracy" },
        { value: "2M+", label: "Documents Processed" },
        { value: "50k+", label: "Active Users" },
        { value: "4.9/5", label: "Customer Rating" },
      ],
      features: [
        {
          title: "Automated Processing",
          description: "Process documents automatically with high accuracy",
          icon: "IconAutomated",
        },
        {
          title: "Real-time Tracking",
          description:
            "Monitor your finances in real-time with detailed insights",
          icon: "IconTracking",
        },
        {
          title: "Secure Platform",
          description: "Enterprise-grade security for your financial data",
          icon: "IconSecurity",
        },
      ],
      footerSections: [
        {
          title: "Product",
          links: ["Features", "Pricing", "Security", "Integrations"],
        },
        {
          title: "Company",
          links: ["About", "Careers", "Contact", "Partners"],
        },
      ],
    };
  },
  components: {
    IconAutomated: {
      template: `
          <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M13 10V3L4 14h7v7l9-11h-7z" fill="currentColor"/>
          </svg>
        `,
    },
    IconTracking: {
      template: `
          <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M9 17v-2M12 17v-4M15 17V9" stroke="currentColor" stroke-width="2"/>
          </svg>
        `,
    },
    IconSecurity: {
      template: `
          <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z" stroke="currentColor" stroke-width="2"/>
          </svg>
        `,
    },
  },
};
</script>

<style>
.animate__animated {
  animation-duration: 1s;
  animation-fill-mode: both;
}

.animate__fadeInLeft {
  animation-name: fadeInLeft;
}

.animate__fadeInRight {
  animation-name: fadeInRight;
}

@keyframes fadeInLeft {
  from {
    opacity: 0;
    transform: translate3d(-100%, 0, 0);
  }
  to {
    opacity: 1;
    transform: translate3d(0, 0, 0);
  }
}

@keyframes fadeInRight {
  from {
    opacity: 0;
    transform: translate3d(100%, 0, 0);
  }
  to {
    opacity: 1;
    transform: translate3d(0, 0, 0);
  }
}
</style>
