<script>
  import { onMount } from "svelte";
  // Import the main module of echarts.
  import * as echarts from "echarts";
  // Render line chart and components.
  onMount(async () => {
    echarts.init(document.getElementById("main")).setOption({
      title: {
        text: "Blocks Diagram"
      },
      tooltip: {},
      animationDurationUpdate: 1500,
      animationEasingUpdate: "quinticInOut",
      series: [
        {
          type: "graph",
          layout: "none",
          symbolSize: 50,
          roam: true,
          symbol: ["rectangle"],
          label: {
            show: true
          },
          edgeSymbol: ["circle", "arrow"],
          edgeSymbolSize: 15,
          edgeLabel: {
            fontSize: 20
          },
          data: [
            {
              name: "Male",
              x: 300,
              y: 300
            },
            {
              name: "Female",
              x: 800,
              y: 300
            },
            {
              name: "God",
              x: 550,
              y: 100
            },
            {
              name: "Birth",
              x: 550,
              y: 500
            }
          ],
          // links: [],
          links: [
            {
              source: "God",
              target: "Male"
            },
            {
              source: "God",
              target: "Female"
            },
            {
              source: "Female",
              target: "Node 4"
            },
            {
              source: "Male",
              target: "Birth"
            },
            {
              source: "Female",
              target: "Birth"
            }
          ],
          lineStyle: {
            opacity: 0.9,
            width: 2,
            curveness: 0
          }
        }
      ]
    });
  });
</script>
  
  <div id="main" style="width: 600px;height:400px;"></div>