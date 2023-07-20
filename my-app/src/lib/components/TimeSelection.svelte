<script lang="ts">
    import Plot from 'svelte-plotly.js';

var xValues = ['A', 'B', 'C', 'D', 'E'];

var yValues = ['W', 'X', 'Y', 'Z'];

var zValues = [
  [0.00, 0.00, 0.75, 0.75, 0.00],
  [0.00, 0.00, 0.75, 0.75, 0.00],
  [0.75, 0.75, 1, 0.75, 0.75],
  [0.00, 0.00, 0.00, 1, 0.00]
];

var colorscaleValue:Plotly.ColorScale = [
  [0, '#3D9970'],
  [1, '#001f3f']
];

var data:Plotly.Data[] = [{
  x: xValues,
  y: yValues,
  z: zValues,
  xgap: 5,
  ygap: 5,
  type: 'heatmap',
  colorscale: colorscaleValue,
  showscale: false
}];

var layout = {
  autosize: true,
  
};

</script>


<Plot
  data={data}
  layout={layout}
/>