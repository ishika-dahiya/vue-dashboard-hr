<template>
  <div
    class="p-2 bg-white divide-y-2 divide-gray-300 border-2 border-gray-300 rounded-lg"
  >
    <div class="flex items-center justify-between pt-5 pb-2 px-2">
      <h3 class="text-lg font-semibold">Hire Funnel</h3>
    </div>
    <div class="p-4">
      <div class="relative mt-4">
        <div class="absolute inset-0 flex items-center">
          <div
            class="w-1/2 h-1 bg-gradient-to-r from-green-500 from-20% via-yellow-500 via-40% to-red-600"
          ></div>
          <div
            class="w-1/2 h-1 bg-gradient-to-r from-red-600 from-10% via-teal-600 via-40% to-purple-600"
          ></div>
        </div>
        <div class="flex items-center justify-evenly w-full ">
          <div class="p-5 rounded-full bg-green-100">
            <div
            class="translate-x-0 bg-green-500 border-4 border-white rounded-full w-4 h-4"
          ></div>
          </div>
          <div class="p-4 rounded-full bg-yellow-100">
            <div
            class="translate-x-0 bg-yellow-500 border-4 border-white rounded-full w-4 h-4"
          ></div>
          </div>
          <div class="p-3 rounded-full bg-red-100">
            <div
            class="translate-x-0 bg-red-500 border-4 border-white rounded-full w-4 h-4"
          ></div>
          </div>
          <div class="p-2 rounded-full bg-teal-100">
            <div
            class="translate-x-0 bg-teal-500 border-4 border-white rounded-full w-4 h-4"
          ></div>
          </div>
          <div class="p-1 rounded-full bg-purple-100">
            <div
            class="translate-x-0 bg-purple-500 border-4 border-white rounded-full w-4 h-4"
          ></div>
          </div>
        </div>
      </div>
      <div class="flex justify-evenly py-6">
        <div class="text-center">
          <div class="font-semibold">499</div>
          <div class="text-gray-500 text-xs">Total Applicant</div>
        </div>
        <div class="text-center">
          <div class="font-semibold">399</div>
          <div class="text-gray-500 text-xs">Filtered</div>
        </div>
        <div class="text-center">
          <div class="font-semibold">299</div>
          <div class="text-gray-500 text-xs">Interviewed</div>
        </div>
        <div class="text-center">
          <div class="font-semibold">199</div>
          <div class="text-gray-500 text-xs">Pre-selected</div>
        </div>
        <div class="text-center">
          <div class="font-semibold">32</div>
          <div class="text-gray-500 text-xs">Hired</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HireFunnel",
};
</script>
