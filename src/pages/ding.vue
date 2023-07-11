<script setup lang="ts">
let money_a = ref(0)

defineOptions({
  name: 'Counter',
})
const counter = createCounter()

const increase_money = () => {
  money_a.value += 10
  counter.inc()
}
</script>

<template>
  <div>
    <ElCard shadow="never">
      <ElSkeleton animated>
        <ElRow :gutter="20" justify="space-between">
          <ElCol :xl="12" :lg="12" :md="12" :sm="24" :xs="24">
            <div class="flex items-center">
              <img
                src="@/assets/imgs/avatar.jpg"
                alt=""
                class="mr-20px h-70px w-70px rounded-[50%]"
              />
              <div>
                <div class="text-20px text-700">Arche</div>
                <div class="mt-10px text-14px text-gray-500">20℃ - 32℃！</div>
              </div>
            </div>
          </ElCol>
          <ElCol :xl="12" :lg="12" :md="12" :sm="24" :xs="24">
            <div class="h-70px flex items-center justify-end <sm:mt-20px">
              <div class="px-8px text-right">
                <div class="mb-20px text-14px text-gray-400">3213123</div>
                <CountTo class="text-20px" :start-val="0" :duration="2600" />
              </div>
              <ElDivider direction="vertical" />
              <div class="px-8px text-right">
                <div class="mb-20px text-14px text-gray-400">2432343</div>
                <CountTo class="text-20px" :start-val="0" :duration="2600" />
              </div>
              <ElDivider direction="vertical" border-style="dashed" />
              <div class="px-8px text-right">
                <div class="mb-20px text-14px text-gray-400">2342rfwefefs</div>
                <CountTo class="text-20px" :start-val="0" :duration="2600" />
              </div>
            </div>
          </ElCol>
        </ElRow>
      </ElSkeleton>
    </ElCard>
  </div>

  <ElRow class="mt-20px" :gutter="20" justify="space-between">
    <ElCol :xl="16" :lg="16" :md="24" :sm="24" :xs="24" class="mb-20px">
      <ElCard shadow="never">
        <template #header>
          <div class="flex justify-between">
            <span>撒旦发射点风格</span>
            <ElLink type="primary" :underline="false">风扇的各项的</ElLink>
          </div>
        </template>
        <ElSkeleton animated>
          <ElRow>
            <ElCol :xl="8" :lg="8" :md="12" :sm="24" :xs="24">
              <ElCard shadow="hover">
                <div class="flex items-center">
                  <Icon :size="25" class="mr-10px" />
                  <span class="text-16px">广大用户电话</span>
                </div>
                <div class="mt-15px text-14px text-gray-400">飞洒地方撒旦</div>
                <div
                  class="mt-20px flex justify-between text-12px text-gray-400"
                >
                  <span>飞洒发顺丰</span>
                  <span>广东富豪的发挥</span>
                </div>
              </ElCard>
            </ElCol>
          </ElRow>
        </ElSkeleton>
      </ElCard>

      <ElCard shadow="never" class="mt-20px">
        <template #header>
          <div class="flex justify-between">
            <span>刚刚回到法国皇帝</span>
            <ElLink type="primary" :underline="false"
              >感豆腐干豆腐干豆腐干</ElLink
            >
          </div>
        </template>
        <ElSkeleton animated>
          <div>
            <div class="flex items-center">
              <img
                src="public/logo.png"
                alt=""
                class="mr-20px h-35px w-35px rounded-[50%]"
              />
              <div>
                <div class="text-14px">广东省分公司的法国队</div>
                <div class="mt-15px text-12px text-gray-400">
                  敢死队敢死队敢死队
                </div>
              </div>
            </div>
            <ElDivider />
          </div>
        </ElSkeleton>
      </ElCard>
    </ElCol>
    <ElCol :xl="8" :lg="8" :md="24" :sm="24" :xs="24" class="mb-20px">
      <ElCard shadow="never">
        <template #header>
          <span>的风格和东方红东方红</span>
        </template>
        <ElSkeleton animated>
          <ElCol
            v-for="item in 9"
            :key="`card-${item}`"
            :xl="12"
            :lg="12"
            :md="12"
            :sm="24"
            :xs="24"
            class="mb-10px"
          >
            <ElLink type="default" :underline="false">
              公司的更好的风格和费用和
            </ElLink>
          </ElCol>
        </ElSkeleton>
      </ElCard>

      <ElCard shadow="never" class="mt-20px">
        <template #header>
          <span>好的凤凰凤凰花</span>
        </template>
        <ElSkeleton animated>
          <Echart :height="400" />
        </ElSkeleton>
      </ElCard>

      <ElCard shadow="never" class="mt-20px">
        <template #header>
          <span>和肉体和东方红东方红</span>
        </template>
        <ElSkeleton animated>
          <ElRow>
            <ElCol :span="12" class="mb-20px">
              <div class="flex items-center">
                <Icon class="mr-10px" />
                <ElLink type="default" :underline="false">
                  {{ money_a }}
                </ElLink>
              </div>
            </ElCol>
          </ElRow>
        </ElSkeleton>
      </ElCard>
    </ElCol>
  </ElRow>
</template>

<style></style>
