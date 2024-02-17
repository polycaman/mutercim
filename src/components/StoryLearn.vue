<script setup>
import { ref } from 'vue';
const story =
  'In einem kleinen Dorf am Rande eines uralten Waldes erzählten sich die Einwohner Geschichten über ein verborgenes Geheimnis. Niemand wagte es, tief in den Wald hineinzugehen, bis eines Tages ein mutiges Mädchen namens Lena beschloss, das Geheimnis zu lüften. Mit nichts als ihrer Neugier ausgestattet, trat sie in den Wald ein. Sie begegnete vielen Herausforderungen und Rätseln, die sie mit Scharfsinn und Mut löste. Schließlich fand sie in der Mitte des Waldes eine versteckte Lichtung, in der ein uralter Baum stand, der leuchtete und warme, sanfte Töne von sich gab. Lena erkannte, dass der Baum das Herz des Waldes war und sein Geheimnis bewahrte. Sie verstand, dass der Wald die Menschen seit Jahrhunderten beschützte und dass seine Geheimnisse nicht zur Zerstörung, sondern zum Schutz aller Lebewesen dienten. Lena kehrte ins Dorf zurück und erzählte von ihren Entdeckungen, und seitdem leben die Dorfbewohner in Harmonie mit dem Wald. Die Geschichte von Lena und dem Geheimnis des alten Waldes wurde zur Legende, die von Generation zu Generation weitergegeben wird, als Erinnerung daran, dass Mut und Neugier uns zu wahren Wundern führen können.';

const storyTranslations = [
  {
    almanca: 'In',
    turkce: 'İçinde',
  },
  {
    almanca: 'einem',
    turkce: 'bir',
  },
  {
    almanca: 'kleinen',
    turkce: 'küçük',
  },
  {
    almanca: 'Dorf',
    turkce: 'köy',
  },
  {
    almanca: 'am',
    turkce: '-de',
  },
  {
    almanca: 'Rande',
    turkce: 'kenarında',
  },
  {
    almanca: 'eines',
    turkce: 'bir',
  },
  {
    almanca: 'uralten',
    turkce: 'antik',
  },
  {
    almanca: 'Waldes',
    turkce: 'ormanın',
  },
  {
    almanca: 'erzählten',
    turkce: 'anlattılar',
  },
  {
    almanca: 'sich',
    turkce: 'kendilerine',
  },
  {
    almanca: 'Einwohner',
    turkce: 'sakinleri',
  },
  {
    almanca: 'Geschichten',
    turkce: 'hikayeler',
  },
  {
    almanca: 'über',
    turkce: 'hakkında',
  },
  {
    almanca: 'verborgenes',
    turkce: 'gizli',
  },
  {
    almanca: 'Geheimnis',
    turkce: 'sır',
  },
  {
    almanca: 'Niemand',
    turkce: 'Kimse',
  },
  {
    almanca: 'wagte',
    turkce: 'cesaret etti',
  },
  {
    almanca: 'es',
    turkce: 'onu',
  },
  {
    almanca: 'tief',
    turkce: 'derin',
  },
  {
    almanca: 'hineinzugehen',
    turkce: 'girmek',
  },
  {
    almanca: 'bis',
    turkce: 'kadar',
  },
  {
    almanca: 'Tages',
    turkce: 'gün',
  },
  {
    almanca: 'mutiges',
    turkce: 'cesur',
  },
  {
    almanca: 'Mädchen',
    turkce: 'kız',
  },
  {
    almanca: 'namens',
    turkce: 'adında',
  },
  {
    almanca: 'Lena',
    turkce: 'Lena',
  },
  {
    almanca: 'beschloss',
    turkce: 'karar verdi',
  },
  {
    almanca: 'lüften',
    turkce: 'açığa çıkarmak',
  },
  {
    almanca: 'Mit',
    turkce: 'İle',
  },
  {
    almanca: 'nichts',
    turkce: 'hiçbir şey',
  },
  {
    almanca: 'als',
    turkce: 'olarak',
  },
  {
    almanca: 'ihrer',
    turkce: 'onun',
  },
  {
    almanca: 'Neugier',
    turkce: 'merak',
  },
  {
    almanca: 'ausgestattet',
    turkce: 'donanımlı',
  },
  {
    almanca: 'trat',
    turkce: 'adım attı',
  },
  {
    almanca: 'begegnete',
    turkce: 'karşılaştı',
  },
  {
    almanca: 'vielen',
    turkce: 'birçok',
  },
  {
    almanca: 'Herausforderungen',
    turkce: 'zorluklar',
  },
  {
    almanca: 'Rätseln',
    turkce: 'bulmacalar',
  },
  {
    almanca: 'Scharfsinn',
    turkce: 'zeka',
  },
  {
    almanca: 'Mut',
    turkce: 'cesaret',
  },
  {
    almanca: 'löste',
    turkce: 'çözdü',
  },
  {
    almanca: 'Schließlich',
    turkce: 'Sonunda',
  },
  {
    almanca: 'fand',
    turkce: 'buldu',
  },
  {
    almanca: 'Mitte',
    turkce: 'ortasında',
  },
  {
    almanca: 'versteckte',
    turkce: 'gizli',
  },
  {
    almanca: 'Lichtung',
    turkce: 'açıklık',
  },
  {
    almanca: 'uralter',
    turkce: 'antik',
  },
  {
    almanca: 'Baum',
    turkce: 'ağaç',
  },
  {
    almanca: 'stand',
    turkce: 'durdu',
  },
  {
    almanca: 'leuchtete',
    turkce: 'parladı',
  },
  {
    almanca: 'warme',
    turkce: 'sıcak',
  },
  {
    almanca: 'sanfte',
    turkce: 'yumuşak',
  },
  {
    almanca: 'Töne',
    turkce: 'tonlar',
  },
  {
    almanca: 'gab',
    turkce: 'verdi',
  },
  {
    almanca: 'erkannte',
    turkce: 'fark etti',
  },
  {
    almanca: 'Herz',
    turkce: 'kalp',
  },
  {
    almanca: 'bewahrte',
    turkce: 'korudu',
  },
  {
    almanca: 'verstand',
    turkce: 'anladı',
  },
  {
    almanca: 'Menschen',
    turkce: 'insanları',
  },
  {
    almanca: 'seit',
    turkce: 'beri',
  },
  {
    almanca: 'Jahrhunderten',
    turkce: 'yüzyıllar',
  },
  {
    almanca: 'beschützte',
    turkce: 'korudu',
  },
  {
    almanca: 'seine',
    turkce: 'onun',
  },
  {
    almanca: 'Geheimnisse',
    turkce: 'sırları',
  },
  {
    almanca: 'nicht',
    turkce: 'değil',
  },
  {
    almanca: 'Zerstörung',
    turkce: 'yıkım',
  },
  {
    almanca: 'sondern',
    turkce: 'ama',
  },
  {
    almanca: 'Schutz',
    turkce: 'koruma',
  },
  {
    almanca: 'aller',
    turkce: 'tüm',
  },
  {
    almanca: 'Lebewesen',
    turkce: 'canlılar',
  },
  {
    almanca: 'dienten',
    turkce: 'hizmet etti',
  },
  {
    almanca: 'kehrte',
    turkce: 'döndü',
  },
  {
    almanca: 'ins',
    turkce: '-e',
  },
  {
    almanca: 'zurück',
    turkce: 'geri',
  },
  {
    almanca: 'erzählte',
    turkce: 'anlattı',
  },
  {
    almanca: 'ihren',
    turkce: 'onun',
  },
  {
    almanca: 'Entdeckungen',
    turkce: 'keşifler',
  },
  {
    almanca: 'seitdem',
    turkce: 'o zamandan beri',
  },
  {
    almanca: 'leben',
    turkce: 'yaşamak',
  },
  {
    almanca: 'Dorfbewohner',
    turkce: 'köy sakinleri',
  },
  {
    almanca: 'Harmonie',
    turkce: 'uyum',
  },
  {
    almanca: 'Geschichte',
    turkce: 'hikaye',
  },
  {
    almanca: 'alten',
    turkce: 'eski',
  },
  {
    almanca: 'wurde',
    turkce: 'oldu',
  },
  {
    almanca: 'Legende',
    turkce: 'efsane',
  },
  {
    almanca: 'Generation',
    turkce: 'nesil',
  },
  {
    almanca: 'weitergegeben',
    turkce: 'aktarıldı',
  },
];
const title = 'Başlamak için Oynat tuşuna bas.';

let synth = window.speechSynthesis;
let pitch = ref(1);
let rate = ref(0.1);
let playText = ref('Oynat');
let storySentences = story.match(/[^.!?]+[.!?]+/g);
let currentReading = {
  text: ref(title),
  maxSentenceIndex: ref(storySentences.length - 1),
  maxWordIndex: ref(0),
  sentenceIndex: ref(0),
  wordIndex: ref(0),
  sentences: [],
  words: [],
  sentence: [],
  word: [],
};

function restart() {
  currentReading = {
    text: ref(title),
    maxSentenceIndex: ref(storySentences.length - 1),
    maxWordIndex: ref(0),
    sentenceIndex: ref(0),
    wordIndex: ref(0),
    sentences: [],
    words: [],
    sentence: [],
    word: [],
  };
  playButtonText('Yeniden Oynat');
  this.synth.cancel();
}

async function playStop() {
  if (this.synth.speaking) {
    playButtonText('Oynat');
    this.synth.cancel();
    return;
  }
  if (
    currentReading.sentenceIndex.value === 0 &&
    currentReading.wordIndex.value === 0
  ) {
    playButtonText('Durdur');
    await startProcessAndSpeakSentences(this.storySentences);
  } else {
    playButtonText('Durdur');
    await continueProcessAndSpeakSentences();
  }
}

async function gameClicked() {
  this.synth.cancel();
  await speakSentence(translateSearch(currentReading.word), 'tr-TR');
  continueProcessAndSpeakSentences();
}

async function startProcessAndSpeakSentences(sentences) {
  currentReading.sentences = sentences;
  for (let i = 0; i < sentences.length; i++) {
    const sentence = sentences[i];
    currentReading.sentence = sentence;
    currentReading.sentenceIndex = i;
    currentReading.words = sentence.split(/\s+|,|\./).filter(Boolean);
    for (let j = 0; j < currentReading.words.length; j++) {
      const word = currentReading.words[j];
      currentReading.word = word;
      currentReading.wordIndex = j;
      currentReading.text.value = `Kelime ${j + 1}: ${word}`;
      await speakSentence(word, 'de-DE');
    }
  }
}

async function continueProcessAndSpeakSentences() {
  for (
    let i = currentReading.sentenceIndex;
    i < currentReading.sentences.length;
    i++
  ) {
    const sentence = currentReading.sentences[i];
    currentReading.sentence = sentence;
    currentReading.sentenceIndex = i;
    currentReading.words = sentence.split(/\s+|,|\./).filter(Boolean);
    for (
      let j = currentReading.wordIndex;
      j < currentReading.words.length;
      j++
    ) {
      const word = currentReading.words[j];
      currentReading.word = word;
      currentReading.wordIndex = j;
      currentReading.text.value = `Word ${j + 1}: ${word}`;
      await speakSentence(word, 'de-DE');
    }
  }
}

function speakSentence(sentence, language) {
  return new Promise((resolve) => {
    let spSynthInstance = new SpeechSynthesisUtterance(sentence);
    spSynthInstance.lang = language;
    spSynthInstance.pitch = pitch.value;
    spSynthInstance.rate = rate.value;
    spSynthInstance.onend = resolve;
    synth.speak(spSynthInstance);
  });
}

function translateSearch(searchText) {
  const sonuc = storyTranslations.find(
    (kelime) => kelime.almanca === searchText
  );
  return sonuc ? sonuc.turkce : 'bilmiyom';
}

function playButtonText(text) {
  playText.value = text;
}
</script>

<template>
  <p v-if="currentReading.sentence.length > 0">
    Cümle {{ currentReading.sentenceIndex + ': ' + currentReading.sentence }}
  </p>
  <p>{{ currentReading.text }}</p>

  <div class="rate-div">
    <div class="label"><b>Hız : </b> &nbsp;&nbsp;{{ rate }}</div>
    <input
      type="range"
      min="0.1"
      max="0.5"
      value="0.1"
      step="0.1"
      v-model="rate"
      @change="speak()"
    />
  </div>
  <div class="pitch-div">
    <div class="label"><b>İncelik : </b> &nbsp;&nbsp;{{ pitch }}</div>
    <input
      type="range"
      min="0"
      max="3"
      value="1"
      step="0.1"
      v-model="pitch"
      @change="speak()"
    />
  </div>
  <br />
  <button id="play" type="button" @click="restart()">Baştan Başla</button>
  <br />
  <br />
  <button id="play" type="button" @click="playStop()">{{ playText }}</button>
  <br />
  <br />
  <button id="game" type="button" @click="gameClicked()">Anlamadım</button>
</template>

<style></style>
