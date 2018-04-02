# react-native-responsive-linechart

<a href="https://badge.fury.io/js/react-native-responsive-linechart"><img src="https://badge.fury.io/js/react-native-responsive-linechart.svg" alt="npm version" height="18"></a>

## Installation

```js
npm install react-native-responsive-linechart
```

```js
import LineChart from 'react-native-responsive-linechart';
```

No need to set an explicit width and height! Percentages or `flex` work just fine.

## Quick example

<a href="url"><img src="https://i.imgur.com/dhcXADa.png" align="middle" width="500" ></a>

```jsx
<LineChart style={{ flex: 1 }} config={config} data={data} />

const data = [-10, -15, 40, 19, 32, 15, 52, 55, 20, 60, 78, 42, 56];
const config = {
  line: {
    strokeWidth: 1,
    strokeColor: '#216D99',
  },
  area: {
    gradientFrom: '#2e86de',
    gradientFromOpacity: 1,
    gradientTo: '#87D3FF',
    gradientToOpacity: 1,
  },
  yAxis: {
    labelColor: '#c8d6e5',
  },
  grid: {
    strokeColor: '#c8d6e5',
    stepSize: 30,
  },
  insetY: 10,
  insetX: 10,
  interpolation: 'spline',
  backgroundColor: '#fff',
}
```

## Reference

### LineChart

| Property        | Type       |  Description  | Example |
| ------------- |-------------| -----| ---- |
| data | array | Your numeric data | [10, 22, 13, 15, 25]
| config | object | Chart configuration object | See next section

### Example Config

```js
const exampleConfig = {
  grid: {
    visible: true,
    backgroundColor: '#fff',
    strokeWidth: 1,
    strokeColor: '#ededed',
    stepSize: 20,
  },
  line: {
    visible: true,
    strokeWidth: 1,
    strokeColor: '#333',
  },
  area: {
    visible: true,
    gradientFrom: '#be2ddd',
    gradientFromOpacity: 1,
    gradientTo: '#e056fd',
    gradientToOpacity: 0.4,
  },
  yAxis: {
    visible: true,
    labelFontSize: 12,
    labelColor: '#777',
    labelFormatter: v => String(v),
  },
  insetY: 10,
  insetX: 10,
  interpolation: 'none',
  backgroundColor: '#fff',
}
```

## More examples

<a href="url"><img src="https://i.imgur.com/0i7LX2n.png" align="middle" width="500" ></a>
```jsx
const data = [-10, -15, 40, 19, 32, 15, 52, 55, 20, 60, 78, 42, 56];
const config = {
  line: {
    visible: true,
    strokeWidth: 1,
    strokeColor: '#54a0ff',
  },
  area: {
    visible: false,
  },
  yAxis: {
    labelColor: '#54a0ff',
  },
  interpolation: 'spline',
  insetY: 10,
  insetX: 10,
}
```

<a href="url"><img src="https://i.imgur.com/r10ncLZ.png" align="middle" width="500" ></a>
```jsx
const data = [-10, -15, 40, 19, 32, 15, 52, 55, 20, 60, 78, 42, 56];
const config = {
  line: {
    visible: true,
    strokeWidth: 2,
    strokeColor: '#341f97',
  },
  area: {
    visible: false,
  },
  yAxis: {
    visible: true,
  },
  grid: {
    stepSize: 15,
  },
  insetY: 10,
  insetX: 10,
}
```


<a href="url"><img src="https://i.imgur.com/gFdef89.png" align="middle" width="500" ></a>
```jsx
const data4 = [-10, -15, 40, 19, 32, 15, 52, 55, 20, 60, 78, 42, 56];
const config4 = { 
  interpolation: 'spline',
  line: { strokeColor: '#be2ddd', strokeWidth: 2 },
  yAxis: { visible: false },
  grid: { visible: false }
}
```

<a href="url"><img src="https://i.imgur.com/rWaUzB3.png" align="middle" width="500" ></a>
```jsx
const data5 = [-10, -15, 40, 19, 32, 15, 52, 55, 20, 60, 78, 42, 56];
const config5 = { 
  interpolation: 'spline',
  area: {
    gradientFrom: '#10ac84',
    gradientFromOpacity: 1,
    gradientTo: '#10ac84',
    gradientToOpacity: 0.4,
  },
  line: {
    visible: false
  }
}```

Note: the cards around the charts are not included.