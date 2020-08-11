<template>
  <div v-if="$vuetify.breakpoint.sm">
  <v-timeline dense style='margin:0vw 6vw;'>
    <v-timeline-item
      v-for="(flow) in flows"
      :key="flow.id"
      :color="flow.color"
      small
    >
      <template v-slot:opposite>
        <span
          :class="`headline font-weight-bold ${flow.color}--text`"
          v-text="flow.num"
        ></span>
      </template>
      
      <div class="py-4">
        <h2 :class="`headline font-weight-light mb-1 ${flow.color}--text`">{{ flow.subtitle }} </h2>
        <div class=" headexp" :key="index">
          {{ flow.exp  }}
        </div>
      </div>
    </v-timeline-item>
  </v-timeline>
  </div>

  <div v-else>
        <v-timeline style='margin:0vw 6vw;'>
    <v-timeline-item
      v-for="(flow) in flows"
      :key="flow.id"
      :color="flow.color"
      small
    >
      <template v-slot:opposite>
        <span
          :class="`headline font-weight-bold ${flow.color}--text`"
          v-text="flow.num"
        ></span>
      </template>
      
      <div class="py-4">
        <h2 :class="`headline font-weight-light mb-1 ${flow.color}--text`">{{ flow.subtitle }} </h2>
        <div class=" headexp" :key="index">
          {{ flow.exp  }}
        </div>
      </div>
    </v-timeline-item>
  </v-timeline>
  </div>

</template>

<script>
  export default {
    data: () => ({
      flows: [
        {
          color: 'cyan',
          num: 'Step1',
          subtitle: '大会エントリー',
          exp: '大会エントリーはTonamelのメソロギア大会ページで行っています。大会リンクはイベントの"エントリーページ"から。大会エントリーにはTwitterアカウントが必要です。1分程で登録/エントリーができます。'
          
        },
        {
          color: 'green',
          num: 'Step2',
          subtitle: '当日チェックイン',
          exp: '大会開始の1時間前よりチェックインを開始します。最終的な参加者を事前に知り、スムーズな大会進行を行うためです。チェックインは大会エントリーページを開くと自動でチェックインをするよう誘導されます。*Tonamelにログインしてください。',
        },
        {
          color: 'pink',
          num: 'Step3',
          subtitle: 'トーナメント表',
          exp: '大会開始時刻になると、トーナメント表が発表されます。Tonamelのメソロギア大会ページからトーナメント表ページにアクセスできます。',
        },
        {
          color: 'amber',
          num: 'Step4',
          subtitle: '試合進行',
          exp: 'トーナメントページで自分の名前を探します。対戦相手とはチャットをすることが可能です。組合せ表の上側がルーム作成、下側が入室をしてください。試合終了後は結果の申請（勝者）と結果の承認（敗者）をお願いします。',
        },
        {
          color: 'orange',
          num: 'Step5',
          subtitle: '賞品受け渡し',
          exp: '大会入賞者につきましては、後日運営者より入賞者のTwitterアカウントにDMにて手続きを行います。賞品は最長1ヶ月以内にはお渡しします。',
        },
      ],
    }),
  }
</script>

<style scoped>
    .headline.headexp{
        margin:0vw 3vw;
    }

    .headline{
        font-size:1vw;
    }
    
</style>