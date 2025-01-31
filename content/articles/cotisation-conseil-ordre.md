+++
title = "Évolution de la cotisation ordinale des médecins"
description = "Évolution du montant de la cotisation annuelle au Conseil de l'Ordre des Médecins de 2001 à 2021, corrigée de l'inflation"
longHtml = true
auteurs = ["Jean-Baptiste FRON"]
date = 2021-12-09T08:59:00+02:00
publishdate = 2022-01-18
lastmod = 2022-01-24
specialites = []
sources = ["CNOM"]
tags = []
draft = false
chart = true
image = false
imageSrc = ""
todo = "valeur C"
+++

### Résumé

La cotisation au Conseil National de l'Ordre des Médecins (CNOM) est **stable sur les 10 dernières années**, avec un montant (corrigé de l'inflation) de 330,2 € contre 335 € en 2021 (et 2022). Elle suit donc la valeur du C, parfaitement stable sur 10 ans.

Sur 20 ans (2001-2021), l'augmentation de la cotisation ordinale atteint presque **20%** (19,4%, corrigés de l'inflation). Sur cette période, le C a augmenté de **8,6%** (22,3€ en 2001). Dès 2002 le C est d'ailleurs à la valeur actuelle (20€ soit l'équivalent 25,2€ de 2021).

### Graphique

<figure>
  <div id="chart" class="border alert mb-4"></div>
  <figcaption>Figure. Montant de la cotisation ordinale des médecins de 2001 à 2021. Valeurs faciales et valeurs corrigées de l'inflation. Dr JB Fron d'après cotisations CNOM.</figcaption>
</figure>
<script>
// https://www.insee.fr/fr/information/2417794
const chartOptions = {
  series: [{
    name: 'Euros courants',
    data: [214, 219, 227, 235, 245, 252, 260, 275, 290, 295, 300, 300, 300, 305, 320, 330, 333, 335, 335, 335, 335]
  }, {
    name: 'Euros 2021',
    data: [66.55, 62.55, 58.97, 54.87, 51.7, 48.3, 45.88, 39.06, 40.91, 36.57, 30.21, 23.88, 21.08, 19.8, 20.64, 20.65, 17.21, 10.92, 7.14, 5.5, 0]
  }],
  chart: { stacked: true },
  title: { text: 'Évolution de la cotisation ordinale des médecins de 2001 à 2021' },
  xaxis: {
    categories: [2001, 2002, 2003, 2004, 2005, 2006, 2007, 2008, 2009, 2010, 2011, 2012, 2013, 2014, 2015, 2016, 2017, 2018, 2019, 2020, 2021],
    tickAmount: 10
  },
  yaxis: [
    {
      title: { text: "Montant (€)" },
      labels: {
        style: { colors: '#757575' }
      },
      decimalsInFloat: 0
    }
  ],
  tooltip: {
    // x: { show: true },
    y: [{
      formatter: function(value) { return `${value} €` }
    },
    {
      formatter: function(value, { series, seriesIndex, dataPointIndex, w }) {
        value += series[0][dataPointIndex];
        Math.round(value);
        return `<strong>${value} €</strong>`;
        }
    }]
  },
  theme: {
    monochrome: { enabled: true }
  }
}
</script>
