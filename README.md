# dataViz 


### COPY THE HTML FROM HERE  --> HTML template with Bootstrap@3.3.1 by CDN
  https://gist.github.com/Pelirrojo/e111662431e642388e57572fca8efb05 
  
  
 
### PASTE IN CODEPEN 
    https://codepen.io/taniabatista/pen/JvQjdv

 
### ADD LIBRARIES UNDER     <!-- Bootstrap -->]

      --> https://cdnjs.com/libraries/nvd3/1.8.5
<link rel="https://cdnjs.cloudflare.com/ajax/libs/nvd3/1.8.5/nv.d3.css">
  
  
  
### ADD STYLE UNDER      <!-- Bootstrap -->
  
    --> https://github.com/novus/nvd3/blob/master/examples/bulletChart.html 
<style>
      text {
          font: 12px sans-serif;
      }
      svg {
          display: block;
      }
      html, body, #chart1, svg {
          margin: 0px;
          padding: 0px;
          height: 100%;
          width: 100%;
      }
  </style>
    
    
    
### ADD SCRIPT UNDER 	 <!-- jQuery (necessary for Bootstrap's JavaScript plugins) -->

    -->  https://cdnjs.com/libraries/d3/3.1.1
<script src="https://cdnjs.cloudflare.com/ajax/libs/d3/3.1.1/d3.js"></script>

    --> https://cdnjs.com/libraries/nvd3/1.8.5
<script src="https://cdnjs.cloudflare.com/ajax/libs/nvd3/1.8.5/nv.d3.js"></script>

 
 
 
### ADD "Grafico Boxplot" class=gallery UNDER     <!-- Include all compiled plugins (below), or include individual files as needed -->

    --> https://github.com/novus/nvd3/blob/master/examples/boxPlotCustomModel.html    
<!-- Grafico boxplot -->
</head>

<body>

<div class="gallery" id="chart1">
    <svg></svg>
</div>     




### ADD SCRIPT INSIDE         /* Here you can put here some magic on Javascript */

      --> https://github.com/novus/nvd3/blob/master/examples/boxPlot.html
    <script>
    nv.addGraph(function() {
      var chart = nv.models.boxPlotChart()
          .x(function(d) { return d.label })
          .staggerLabels(true)
          .maxBoxWidth(75) // prevent boxes from being incredibly wide
          .yDomain([0, 500])
          ;
      d3.select('#chart1 svg')
          .datum(exampleData())
          .call(chart);
      nv.utils.windowResize(chart.update);
      return chart;
    });
    function exampleData() {
     return  [
        {
          label: "Sample A",
          values: {
            Q1: 120,
            Q2: 150,
            Q3: 200,
            whisker_low: 115,
            whisker_high: 210,
            outliers: [50, 100, 225]
          },
        },
        {
          label: "Sample B",
          values: {
            Q1: 300,
            Q2: 350,
            Q3: 400,
            whisker_low: 225,
            whisker_high: 425,
            outliers: [175]
          },
        },
        {
          label: "Sample C",
          values: {
            Q1: 50,
            Q2: 100,
            Q3: 125,
            whisker_low: 25,
            whisker_high: 175,
            outliers: [0]
          },
        }
      ];
    }
</script>
