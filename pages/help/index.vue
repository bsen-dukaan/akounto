<template>
  <div class="min-h-screen bg-white">
    <!-- Navbar -->
    <nav class="bg-white shadow-sm">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="h-16 flex items-center">
          <a href="/" class="flex-shrink-0">
            <img
              class="h-8 w-auto"
              src="https://www.akounto.com/images/logo.svg"
              alt="Your Company"
            />
          </a>
        </div>
      </div>
    </nav>
    <div class="max-w-4xl mx-auto px-4 py-16">
      <!-- Disconnected Message Section -->
      <div class="text-center mb-24">
        <h1 class="text-4xl font-bold mb-8 text-gray-900">
          QuickBooks Disconnected
        </h1>
        <p class="text-lg mb-4 text-gray-600">
          Your QuickBooks integration has been disconnected. You will no longer
          to be able to send invoices directly to your QuickBooks account from
          Tradify.
        </p>
        <p class="text-lg text-gray-600">
          If you'd like to re-connect Tradify and your QuickBooks account,
          <NuxtLink
            to="/account/integrations"
            class="text-indigo-600 hover:text-indigo-700 hover:underline"
          >
            click here
          </NuxtLink>
          to view our help guide.
        </p>
      </div>

      <!-- Help Section -->
      <div class="text-center mb-16">
        <h2 class="text-3xl text-indigo-600 mb-12">We're here to help</h2>

        <!-- Support Options -->
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
          <!-- Help Centre -->
          <div class="bg-gray-200 p-6 rounded-lg shadow-sm">
            <h3 class="text-xl text-indigo-600 font-semibold mb-4">
              Help Centre
            </h3>
            <p class="text-gray-600">
              Read help articles, setup guides, tips & resources to help you
              make the most of Tradify.
            </p>
          </div>

          <!-- Getting Setup -->
          <div class="bg-gray-200 p-6 rounded-lg shadow-sm">
            <h3 class="text-xl text-indigo-600 font-semibold mb-4">
              Getting Setup
            </h3>
            <p class="text-gray-600">
              See how easy it is to get setup & booking jobs in 6 steps.
            </p>
          </div>

          <!-- Free Training -->
          <div class="bg-gray-200 p-6 rounded-lg shadow-sm">
            <h3 class="text-xl text-indigo-600 font-semibold mb-4">
              Free Live Training
            </h3>
            <p class="text-gray-600">
              Our trade mad setup specialists will get you up and running right
              away.
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
definePageMeta({
  layout: false,
});
</script>
