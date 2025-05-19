<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Weight Comparison Chart</title>
  <!-- Chart.js CDN -->
  <script src="https://cdn.jsdelivr.net/npm/chart.js@4.4.3/dist/chart.umd.min.js"></script>
  <style>
    body {
      background-color: #f5f5f5;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
      font-family: Arial, sans-serif;
    }
    #weightChart {
      max-width: 800px;
      max-height: 600px;
      background-color: #fff;
      border: 1px solid #ccc;
      padding: 20px;
    }
  </style>
</head>
<body>
  <canvas id="weightChart"></canvas>

  <script>
    document.addEventListener('DOMContentLoaded', () => {
      const ctx = document.getElementById('weightChart').getContext('2d');

      new Chart(ctx, {
        type: 'bar',
        data: {
          labels: ['Earth', 'Mars', 'Moon'],
          datasets: [{
            label: 'Weight of 40 kg (N)',
            data: [392, 148.4, 64.8],
            backgroundColor: ['#36A2EB', '#FF6384', '#FFCE56'],
            borderColor: ['#2A80B9', '#CC4F6B', '#CCA300'],
            borderWidth: 1
          }]
        },
        options: {
          responsive: true,
          maintainAspectRatio: true,
          animation: {
            duration: 4000,
            easing: 'easeInOutQuad',
            delay: (context) => context.dataIndex * 1000
          },
          scales: {
            y: {
              beginAtZero: true,
              title: {
                display: true,
                text: 'Weight (Newtons)',
                font: { size: 16 }
              },
              ticks: {
                font: { size: 12 }
              },
              grid: {
                color: '#e0e0e0'
              }
            },
            x: {
              title: {
                display: true,
                text: 'Celestial Body',
                font: { size: 16 }
              },
              ticks: {
                font: { size: 12 }
              },
              grid: {
                display: false
              }
            }
          },
          plugins: {
            title: {
              display: true,
              text: 'Weight of 40 kg on Different Celestial Bodies',
              font: { size: 18 },
              padding: 15
            },
            legend: {
              display: true,
              position: 'top',
              labels: {
                font: { size: 12 }
              }
            },
            tooltip: {
              enabled: true,
              backgroundColor: 'rgba(0,0,0,0.8)',
              titleFont: { size: 12 },
              bodyFont: { size: 10 }
            }
          }
        }
      });
    });
  </script>
</body>
</html>
