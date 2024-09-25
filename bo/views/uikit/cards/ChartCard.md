# Documentazione del Componente `ChartCard.vue`

## Descrizione

`ChartCard.vue` è un componente di visualizzazione dei dati che combina un grafico con informazioni riassuntive. Supporta diversi tipi di grafici e presenta opzioni personalizzabili per la visualizzazione.

## Props

| Nome               | Tipo      | Richiesta | Valore Predefinito | Descrizione                                                        |
| ------------------ | --------- | --------- | ------------------ | ------------------------------------------------------------------ |
| `chartType`        | `String`  | Sì        | `'pie'`            | Tipo di grafico da visualizzare (es. 'bar', 'line', 'pie').        |
| `chartData`        | `Array`   | Sì        | -                  | Dati da visualizzare nel grafico.                                  |
| `chartLabels`      | `Array`   | Sì        | -                  | Etichette da visualizzare sul grafico.                             |
| `title`            | `String`  | No        | `'Data Overview'`  | Titolo del grafico.                                                |
| `mainValue`        | `Number`  | No        | `null`             | Valore principale da visualizzare sotto il grafico.                |
| `mainLabel`        | `String`  | No        | `'Value'`          | Etichetta per il valore principale.                                |
| `changeValue`      | `Number`  | No        | `null`             | Valore del cambiamento percentuale rispetto al periodo precedente. |
| `positiveChange`   | `Boolean` | No        | `true`             | Indica se il cambiamento è positivo o negativo.                    |
| `options`          | `Object`  | No        | `{}`               | Opzioni per personalizzare il grafico.                             |
| `useDefaultColors` | `Boolean` | No        | `true`             | Se `true`, utilizza i colori predefiniti.                          |

## Esempio di Utilizzo

```vue
<template>
  <ChartCard
    chartType="pie"
    :chartData="[10, 20, 30]"
    :chartLabels="['Red', 'Blue', 'Green']"
    title="Sales Overview"
    :mainValue="60"
    mainLabel="Total Sales"
    :changeValue="5"
    :positiveChange="true"
    :options="{ responsive: true }"
    :useDefaultColors="false"
  />
</template>
```

# Documentazione del Componente `BaseChart.vue`

## Descrizione

`BaseChart.vue` è un componente di supporto per il rendering di vari tipi di grafici utilizzando una libreria di grafici. Gestisce i dati e le opzioni di configurazione per il grafico.

## Props

| Nome               | Tipo      | Richiesta | Valore Predefinito | Descrizione                                                 |
| ------------------ | --------- | --------- | ------------------ | ----------------------------------------------------------- |
| `type`             | `String`  | Sì        | -                  | Tipo di grafico da visualizzare (es. 'bar', 'line', 'pie'). |
| `data`             | `Object`  | Sì        | -                  | Dati da visualizzare nel grafico.                           |
| `options`          | `Object`  | No        | `{}`               | Opzioni di configurazione del grafico.                      |
| `useDefaultColors` | `Boolean` | No        | `true`             | Se `true`, utilizza colori predefiniti per il grafico.      |

## Esempio di Utilizzo

```vue
<template>
  <BaseChart
    type="bar"
    :data="chartData"
    :options="chartOptions"
    :useDefaultColors="true"
  />
</template>

<script setup>
import { ref } from "vue";

const chartData = ref({
  labels: ["January", "February", "March"],
  datasets: [
    {
      label: "Sales",
      data: [30, 50, 40],
      backgroundColor: ["#FF6384", "#36A2EB", "#FFCE56"],
    },
  ],
});

const chartOptions = ref({
  responsive: true,
  maintainAspectRatio: false,
});
</script>
```

## Note

- Assicurati di importare correttamente i componenti nei file in cui intendi utilizzarli.
- Controlla eventuali dipendenze necessarie per il funzionamento dei grafici, come le librerie di grafico.

## Conclusioni

Questi componenti offrono un modo flessibile e personalizzabile per visualizzare i dati all'interno di un'applicazione Vue.js. La loro configurabilità permette di adattarli facilmente a diverse esigenze di visualizzazione.
