<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>國泰人壽滿溢寶醫療險分析報告</title>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/apexcharts"></script>
    <style>
        body {
            font-family: '微軟正黑體', 'Microsoft JhengHei', Arial, sans-serif;
            color: #333;
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
            background-color: #f9f9f9;
        }
        .header {
            text-align: center;
            margin-bottom: 40px;
            padding: 30px;
            background: linear-gradient(135deg, #1e5799 0%,#207cca 51%,#2989d8 100%);
            color: white;
            border-radius: 10px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
        }
        .section {
            background: white;
            padding: 25px;
            margin-bottom: 30px;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.05);
        }
        .highlight-box {
            background: linear-gradient(135deg, #f6d365 0%, #fda085 100%);
            color: white;
            padding: 20px;
            border-radius: 10px;
            margin: 20px 0;
            text-align: center;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
        }
        .highlight-number {
            font-size: 3em;
            font-weight: bold;
            margin: 10px 0;
        }
        .chart-container {
            position: relative;
            height: 400px;
            margin: 20px 0 40px 0;
        }
        .chart-title {
            text-align: center;
            font-size: 1.4em;
            margin-bottom: 15px;
            color: #1e5799;
        }
        .benefits-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin: 30px 0;
        }
        .benefit-card {
            background: #fff;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.05);
            transition: transform 0.3s ease;
        }
        .benefit-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 6px 15px rgba(0,0,0,0.1);
        }
        .benefit-icon {
            font-size: 2.5em;
            color: #1e5799;
            margin-bottom: 15px;
        }
        .comparison-table {
            width: 100%;
            border-collapse: collapse;
            margin: 30px 0;
        }
        .comparison-table th, .comparison-table td {
            padding: 15px;
            text-align: center;
            border: 1px solid #ddd;
        }
        .comparison-table th {
            background-color: #1e5799;
            color: white;
        }
        .comparison-table tr:nth-child(even) {
            background-color: #f2f2f2;
        }
        .highlight-cell {
            background-color: #fffde7;
            font-weight: bold;
        }
        .customer-persona {
            display: flex;
            align-items: center;
            margin-bottom: 30px;
            padding: 20px;
            background: #f3f4f6;
            border-radius: 10px;
        }
        .persona-icon {
            font-size: 3em;
            margin-right: 20px;
            color: #1e5799;
        }
        .cta-section {
            text-align: center;
            padding: 40px;
            background: linear-gradient(135deg, #1e5799 0%,#207cca 51%,#2989d8 100%);
            color: white;
            border-radius: 10px;
            margin-top: 40px;
        }
        .cta-button {
            display: inline-block;
            padding: 15px 30px;
            background-color: white;
            color: #1e5799;
            text-decoration: none;
            border-radius: 5px;
            font-weight: bold;
            margin-top: 20px;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 15px rgba(0,0,0,0.2);
        }
        .advantage-list {
            list-style-type: none;
            padding-left: 0;
        }
        .advantage-list li {
            padding: 10px 0;
            position: relative;
            padding-left: 30px;
        }
        .advantage-list li:before {
            content: "✓";
            position: absolute;
            left: 0;
            color: #4CAF50;
            font-weight: bold;
        }
        @media (max-width: 768px) {
            .benefits-grid {
                grid-template-columns: 1fr;
            }
            .chart-container {
                height: 300px;
            }
        }
    </style>
</head>
<body>
    <div class="header">
        <h1>國泰人壽滿溢寶醫療險 - 精英分析報告</h1>
        <p>保費返還、終身保障、醫療防護一次擁有的頂級保單</p>
    </div>

    <div class="section">
        <h2>滿溢寶醫療險 - 前所未有的三重保障</h2>
        <div class="benefits-grid">
            <div class="benefit-card">
                <div class="benefit-icon">💰</div>
                <h3>繳費15年，保障終身</h3>
                <p>只需繳納15年保費，享受終身醫療保障，無須擔心高齡後保費調漲風險。</p>
            </div>
            <div class="benefit-card">
                <div class="benefit-icon">🏥</div>
                <h3>12項重大傷病全面保障</h3>
                <p>涵蓋重大疾病與傷病，為您的健康提供全方位守護。</p>
            </div>
            <div class="benefit-card">
                <div class="benefit-icon">♻️</div>
                <h3>期滿返還所有保費</h3>
                <p>25年後返還100%已繳保費，相當於以0成本獲得終身保障。</p>
            </div>
        </div>

        <div class="highlight-box">
            <p>0歲投保範例：每月僅需</p>
            <div class="highlight-number">NT$ 2,900</div>
            <p>15年後返還約<strong>NT$ 500,000</strong>，並獲得價值<strong>NT$ 780,000</strong>的終身醫療保障</p>
        </div>
    </div>

    <div class="section">
        <h2>滿溢寶醫療險 - 投資報酬分析</h2>
        
        <div>
            <div class="chart-title">不同年齡投保費率比較</div>
            <div class="chart-container">
                <canvas id="ageComparisonChart"></canvas>
            </div>
        </div>

        <div>
            <div class="chart-title">15年保費 vs 終身保障價值</div>
            <div class="chart-container">
                <canvas id="valueComparisonChart"></canvas>
            </div>
        </div>

        <div>
            <div class="chart-title">投資回報時間軸</div>
            <div class="chart-container">
                <div id="timelineChart"></div>
            </div>
        </div>
    </div>

    <div class="section">
        <h2>同業保單比較</h2>
        
        <table class="comparison-table">
            <thead>
                <tr>
                    <th>功能項目</th>
                    <th>國泰人壽<br>滿溢寶醫療險</th>
                    <th>A公司<br>醫療保險</th>
                    <th>B公司<br>醫療保險</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>繳費年期</td>
                    <td class="highlight-cell">15年</td>
                    <td>20年</td>
                    <td>30年</td>
                </tr>
                <tr>
                    <td>保障期間</td>
                    <td class="highlight-cell">終身</td>
                    <td>終身</td>
                    <td>到80歲</td>
                </tr>
                <tr>
                    <td>保費返還</td>
                    <td class="highlight-cell">100%</td>
                    <td>75%</td>
                    <td>無</td>
                </tr>
                <tr>
                    <td>重大傷病保障</td>
                    <td class="highlight-cell">12項</td>
                    <td>8項</td>
                    <td>5項</td>
                </tr>
                <tr>
                    <td>0歲投保月繳保費</td>
                    <td class="highlight-cell">NT$ 2,900</td>
                    <td>NT$ 3,600</td>
                    <td>NT$ 3,200</td>
                </tr>
                <tr>
                    <td>投保年齡範圍</td>
                    <td class="highlight-cell">0-55歲</td>
                    <td>20-50歲</td>
                    <td>0-45歲</td>
                </tr>
            </tbody>
        </table>

        <div class="chart-title">保障內容對比</div>
        <div class="chart-container">
            <canvas id="coverageComparisonChart"></canvas>
        </div>
    </div>

    <div class="section">
        <h2>滿溢寶醫療險的絕佳優勢</h2>
        
        <ul class="advantage-list">
            <li><strong>零成本保障</strong> - 25年後全額退還所有已繳保費，相當於免費獲得醫療保障</li>
            <li><strong>及早投保優惠</strong> - 年齡越小，保費越低，0歲投保可獲得最優惠費率</li>
            <li><strong>有限繳費無限保障</strong> - 僅需繳納15年保費，即可獲得終身醫療保障</li>
            <li><strong>高額醫療保障</strong> - 提供超過原始保費投入1.5倍以上的醫療保障價值</li>
            <li><strong>規劃靈活</strong> - 同時滿足儲蓄、教育金、退休金與醫療保障多重需求</li>
            <li><strong>長照替代方案</strong> - 比專業長照險更經濟實惠的保障選擇</li>
        </ul>
    </div>

    <div class="section">
        <h2>適合的客戶類型</h2>
        
        <div class="customer-persona">
            <div class="persona-icon">👶</div>
            <div>
                <h3>新生兒與幼兒父母</h3>
                <p>為孩子規劃教育基金同時提供終身健康保障，0歲投保享最優惠費率，15年後返還的保費可作為子女教育金。</p>
            </div>
        </div>
        
        <div class="customer-persona">
            <div class="persona-icon">👨‍👩‍👧</div>
            <div>
                <h3>有儲蓄需求的中年家長</h3>
                <p>一份保單同時滿足儲蓄與健康保障需求，無需額外購買其他醫療險，15年保費投入，終身受益。</p>
            </div>
        </div>
        
        <div class="customer-persona">
            <div class="persona-icon">👵</div>
            <div>
                <h3>規劃退休金與長照需求者</h3>
                <p>替代高昂的長照險，以更實惠的方式獲得終身醫療保障，期滿返還的保費可作為額外退休金。</p>
            </div>
        </div>
    </div>

    <div class="cta-section">
        <h2>為您與家人的未來投資</h2>
        <p>國泰人壽滿溢寶醫療險 - 一份讓您無後顧之憂的全方位保障</p>
        <p>現在投保，讓每一分保費都成為您將來的資產與保障</p>
        <a href="#" class="cta-button">立即諮詢專業顧問</a>
    </div>

    <script>
        // 年齡與保費關係圖
        const ageCtx = document.getElementById('ageComparisonChart').getContext('2d');
        const ageChart = new Chart(ageCtx, {
            type: 'bar',
            data: {
                labels: ['0歲', '10歲', '20歲', '30歲', '40歲', '50歲'],
                datasets: [{
                    label: '年繳保費 (台幣)',
                    data: [32682, 37000, 42000, 50000, 65000, 83000],
                    backgroundColor: 'rgba(30, 87, 153, 0.7)',
                    borderColor: 'rgba(30, 87, 153, 1)',
                    borderWidth: 1
                }]
            },
            options: {
                responsive: true,
                maintainAspectRatio: false,
                scales: {
                    y: {
                        beginAtZero: true,
                        title: {
                            display: true,
                            text: '年繳保費 (新台幣)'
                        }
                    },
                    x: {
                        title: {
                            display: true,
                            text: '投保年齡'
                        }
                    }
                },
                plugins: {
                    tooltip: {
                        callbacks: {
                            label: function(context) {
                                return `年繳保費: NT$ ${context.raw.toLocaleString()}`;
                            }
                        }
                    }
                }
            }
        });

        // 保費vs保障價值對比
        const valueCtx = document.getElementById('valueComparisonChart').getContext('2d');
        const valueChart = new Chart(valueCtx, {
            type: 'bar',
            data: {
                labels: ['15年總繳保費', '期滿返還金額', '醫療保障價值'],
                datasets: [{
                    label: '金額 (台幣)',
                    data: [500000, 500000, 780000],
                    backgroundColor: [
                        'rgba(255, 159, 64, 0.7)',
                        'rgba(75, 192, 192, 0.7)',
                        'rgba(153, 102, 255, 0.7)'
                    ],
                    borderColor: [
                        'rgba(255, 159, 64, 1)',
                        'rgba(75, 192, 192, 1)',
                        'rgba(153, 102, 255, 1)'
                    ],
                    borderWidth: 1
                }]
            },
            options: {
                responsive: true,
                maintainAspectRatio: false,
                scales: {
                    y: {
                        beginAtZero: true,
                        title: {
                            display: true,
                            text: '金額 (新台幣)'
                        }
                    }
                },
                plugins: {
                    tooltip: {
                        callbacks: {
                            label: function(context) {
                                return `金額: NT$ ${context.raw.toLocaleString()}`;
                            }
                        }
                    }
                }
            }
        });

        // 保障內容對比
        const coverageCtx = document.getElementById('coverageComparisonChart').getContext('2d');
        const coverageChart = new Chart(coverageCtx, {
            type: 'radar',
            data: {
                labels: ['重大傷病保障', '保費返還', '繳費便利性', '保障期限', '投保年齡範圍', '每月保費'],
                datasets: [
                    {
                        label: '國泰人壽滿溢寶',
                        data: [95, 100, 90, 100, 90, 85],
                        backgroundColor: 'rgba(30, 87, 153, 0.2)',
                        borderColor: 'rgba(30, 87, 153, 1)',
                        pointBackgroundColor: 'rgba(30, 87, 153, 1)',
                        borderWidth: 2
                    },
                    {
                        label: 'A公司醫療險',
                        data: [70, 75, 70, 100, 65, 60],
                        backgroundColor: 'rgba(255, 99, 132, 0.2)',
                        borderColor: 'rgba(255, 99, 132, 1)',
                        pointBackgroundColor: 'rgba(255, 99, 132, 1)',
                        borderWidth: 2
                    },
                    {
                        label: 'B公司醫療險',
                        data: [50, 0, 40, 70, 80, 70],
                        backgroundColor: 'rgba(255, 206, 86, 0.2)',
                        borderColor: 'rgba(255, 206, 86, 1)',
                        pointBackgroundColor: 'rgba(255, 206, 86, 1)',
                        borderWidth: 2
                    }
                ]
            },
            options: {
                responsive: true,
                maintainAspectRatio: false,
                scales: {
                    r: {
                        angleLines: {
                            display: true
                        },
                        suggestedMin: 0,
                        suggestedMax: 100
                    }
                }
            }
        });

        // 時間軸圖表
        const options = {
            series: [
                {
                    name: '累積保費',
                    data: [
                        { x: '第1年', y: 32682 },
                        { x: '第5年', y: 163410 },
                        { x: '第10年', y: 326820 },
                        { x: '第15年', y: 490230 },
                        { x: '第25年', y: 490230 }
                    ]
                },
                {
                    name: '保障價值',
                    data: [
                        { x: '第1年', y: 780000 },
                        { x: '第5年', y: 780000 },
                        { x: '第10年', y: 780000 },
                        { x: '第15年', y: 780000 },
                        { x: '第25年', y: 780000 }
                    ]
                },
                {
                    name: '返還保費',
                    data: [
                        { x: '第1年', y: 0 },
                        { x: '第5年', y: 0 },
                        { x: '第10年', y: 0 },
                        { x: '第15年', y: 0 },
                        { x: '第25年', y: 490230 }
                    ]
                }
            ],
            chart: {
                height: 400,
                type: 'line',
                zoom: {
                    enabled: false
                }
            },
            dataLabels: {
                enabled: false
            },
            stroke: {
                curve: 'straight',
                width: [3, 3, 4],
                dashArray: [0, 0, 5]
            },
            colors: ['#FF9F40', '#9966FF', '#4BC0C0'],
            title: {
                text: '滿溢寶醫療險 - 15年期投資回報時間軸',
                align: 'center'
            },
            markers: {
                size: 5
            },
            xaxis: {
                title: {
                    text: '時間'
                }
            },
            yaxis: {
                title: {
                    text: '金額 (新台幣)'
                },
                labels: {
                    formatter: function (value) {
                        return value.toLocaleString() + " 元";
                    }
                }
            },
            legend: {
                position: 'top',
                horizontalAlign: 'right'
            },
            annotations: {
                points: [{
                    x: '第15年',
                    y: 490230,
                    marker: {
                        size: 6,
                        fillColor: '#ff4560',
                        strokeColor: '#fff',
                        radius: 3
                    },
                    label: {
                        text: '繳費完成',
                        offsetY: 0,
                        style: {
                            color: '#fff',
                            background: '#ff4560'
                        }
                    }
                },
                {
                    x: '第25年',
                    y: 490230,
                    marker: {
                        size: 6,
                        fillColor: '#4BC0C0',
                        strokeColor: '#fff',
                        radius: 3
                    },
                    label: {
                        text: '全額返還',
                        offsetY: 0,
                        style: {
                            color: '#fff',
                            background: '#4BC0C0'
                        }
                    }
                }]
            }
        };

        const timelineChart = new ApexCharts(document.querySelector("#timelineChart"), options);
        timelineChart.render();
    </script>
</body>
</html>
