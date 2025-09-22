<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>报告查询系统 - PDF下载解决方案</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #1a2980, #26d0ce);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
            color: #333;
        }
        
        .container {
            background-color: white;
            border-radius: 16px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.2);
            width: 100%;
            max-width: 900px;
            overflow: hidden;
        }
        
        .header {
            background: linear-gradient(to right, #1a2980, #26d0ce);
            color: white;
            padding: 30px;
            text-align: center;
        }
        
        .header h1 {
            font-size: 2.2rem;
            margin-bottom: 10px;
            font-weight: 700;
        }
        
        .header p {
            font-size: 1.1rem;
            opacity: 0.9;
        }
        
        .content {
            padding: 30px;
        }
        
        .search-section {
            margin-bottom: 30px;
            text-align: center;
        }
        
        .input-group {
            margin-bottom: 20px;
        }
        
        .input-group label {
            display: block;
            margin-bottom: 10px;
            font-weight: 600;
            color: #2c3e50;
            font-size: 1.1rem;
        }
        
        .input-container {
            display: flex;
            width: 100%;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 3px 10px rgba(0, 0, 0, 0.1);
            max-width: 600px;
            margin: 0 auto;
        }
        
        input[type="text"] {
            flex: 1;
            padding: 15px 20px;
            border: none;
            background: #f9fafc;
            font-size: 1rem;
            color: #2c3e50;
        }
        
        input[type="text"]:focus {
            background: #fff;
            outline: none;
            box-shadow: inset 0 0 0 2极px #26d0ce;
        }
        
        input[type="text"]::placeholder {
            color: #aab7c5;
        }
        
        button {
            background: linear-gradient(to right, #1a2980, #26d0ce);
            color: white;
            border: none;
            padding: 0 25px;
            cursor: pointer;
            font-size: 1rem;
            font-weight: 600;
            transition: all 0.3s;
        }
        
        button:hover {
            background: linear-gradient(to right, #2234b8, #2de0de);
        }
        
        button i {
            margin-right: 8px;
        }
        
        .results-section {
            display: none;
            background-color: #f8fafd;
            border-radius: 12px;
            padding: 25px;
            margin-top: 25px;
            border: 1px solid #e1e8f0;
        }
        
        .results-section h2 {
            color: #1a2980;
            margin-bottom: 20px;
            padding-bottom: 15px;
            border-bottom: 2px solid #e6ecf5;
            font-size: 1.5rem;
            display: flex;
            align-items: center;
        }
        
        .results-section h2 i {
            margin-right: 10px;
        }
        
        .report-details {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
            margin-bottom: 25px;
        }
        
        .detail-item {
            padding: 15px;
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 2px 8px rgba(0,0,0,0.05);
            border-left: 4px solid #26d0ce;
        }
        
        .detail-item h3 {
            font-size: 0.9rem;
            color: #7b8a9b;
            margin-bottom: 8px;
        }
        
        .detail-item p {
            font-size: 1.1rem;
            font-weight: 600;
            color: #2c3e50;
        }
        
        .download-section {
            margin-top: 20px;
            text-align: center;
        }
        
        .download-btn {
            background: linear-gradient(to right, #ff416c, #ff4b2b);
            color: white;
            border: none;
            padding: 15px 35px;
            border-radius: 8px;
            cursor: pointer;
            font-size: 1.1rem;
            font-weight: 600;
            transition: all 0.3s;
            display: inline-flex;
            align-items: center;
            box-shadow: 0 4px 10px rgba(255, 75, 43, 0.3);
        }
        
        .download-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 15px rgba(255, 75, 43, 0.4);
        }
        
        .download-btn i {
            margin-right: 10px;
        }
        
        .footer {
            text-align: center;
            padding: 20px;
            background-color: #f8f9fa;
            color: #6c757d;
            font-size: 0.9rem;
            border-top: 1px solid #e9ecef;
        }
        
        .status-message {
            padding: 12px;
            border-radius: 6px;
            margin-top: 15px;
            display: none;
            font-weight: 500;
        }
        
        .status-message.success {
            background-color: #d4edda;
            color: #155724;
            border: 1px solid #c3e6cb;
        }
        
        .status-message.error {
            background-color: #f8d7da;
            color: #721c24;
            border: 1px solid #f5c6cb;
        }
        
        @media (max-width: 768px) {
            .header {
                padding: 20px;
            }
            
            .header h1 {
                font-size: 1.8rem;
            }
            
            .content {
                padding: 20px;
            }
            
            .input-container {
                flex-direction: column;
                box-shadow: none;
            }
            
            input[type="极text"] {
                border-radius: 8px;
                margin-bottom: 10px;
                box-shadow: 0 2px 6px rgba(0, 0, 0, 0.1);
            }
            
            button {
                border-radius: 8px;
                padding: 12px;
                width: 100%;
            }
            
            .report-details {
                grid-template-columns: 1fr;
            }
            
            .results-section {
                padding: 20px;
            }
            
            .download-btn {
                width: 100%;
                justify-content: center;
            }
        }
        
        .support-info {
            text-align: center;
            margin-top: 20px;
            padding: 15px;
            background-color: #f0f7ff;
            border-radius: 8px;
            border-left: 4px solid #1a2980;
        }
        
        .support-info p {
            color: #4a6fa5;
            font-size: 0.95rem;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1><i class="fas fa-file-alt"></i> 报告查询系统</h1>
            <p>输入报告编号查询相关报告信息</p>
        </div>
        
        <div class="content">
            <div class="search-section">
                <div class="input-group">
                    <label for="report-number">输入报告编号</label>
                    <div class="input-container">
                        <input type="text" id="report-number" placeholder="请输入报告编号..." autocomplete="off">
                        <button id="search-btn"><i class="fas fa-search"></i> 查询</button>
                    </div>
                </div>
            </div>
            
            <div class="results-section" id="results">
                <h2><i class="fas fa-file-pdf"></i> 报告详情</h2>
                <div class="report-details">
                    <div class="detail-item">
                        <h3>报告编号</h3>
                        <p id="rep-number">-</p>
                    </div>
                    <div class="detail-item">
                        <h3>委托单位</h3>
                        <p id="rep-client">-</p>
                    </div>
                    <div class="detail-item">
                        <h3>样品名称</h3>
                        <p id="rep-sample">-</p>
                    </div>
                    <div class="detail-item">
                        <h3>报告日期</h3>
                        <p id="rep-date">-</p>
                    </div>
                </div>
                
                <div class="download-section">
                    <button class="download-btn" id="download-btn">
                        <i class="fas fa-download"></极i> 下载完整报告 (PDF)
                    </button>
                </div>
                
                <div class="status-message" id="status-message"></div>
            </div>
            
            <div class="support-info">
                <p>2025报告查询系统 | 专业技术检测服务</p>
            </div>
        </div>
        
        <div class="footer">
            <p>© 2025 报告查询系统 | 版权所有</p>
        </div>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const searchBtn = document.getElementById('search-btn');
            const reportInput = document.getElementById('report-number');
            const resultsSection = document.getElementById('results');
            const downloadBtn = document.getElementById('download-btn');
            const statusMessage = document.getElementById('status-message');
            
            // 报告数据
            const reports = {
                'BV2025TC106691805': {
                    number: 'BV2025TC106691805',
                    client: '河北省司法厅',
                    sample: '国徽（行政执法、监督证）',
                    date: '2025年09月18日'
                },
                'BV2025TC106691956': {
                    number: 'BV2025TC106691956',
                    client: '河北省司法厅',
                    sample: '识别卡(监督证)',
                    date: '2025年09月22日'
                }
            };
            
            // 查询按钮点击事件
            searchBtn.addEventListener('click', function() {
                const reportId = reportInput.value.trim();
                
                if (!reportId) {
                    showStatus('请输入报告编号', 'error');
                    reportInput.focus();
                    return;
                }
                
                // 检查报告是否存在
                if (reports[reportId]) {
                    // 更新结果区域
                    document.getElementById('rep-number').textContent = reports[reportId].number;
                    document.getElementById('rep-client').textContent = reports[reportId].client;
                    document.getElementById('rep-sample').textContent = reports[reportId].sample;
                    document.getElementById('rep-date').textContent = reports[reportId].date;
                    
                    // 显示结果
                    resultsSection.style.display = 'block';
                    
                    // 滚动到结果区域
                    resultsSection.scrollIntoView({ behavior: 'smooth' });
                    
                    showStatus('找到报告，点击下载按钮生成PDF', 'success');
                } else {
                    showStatus('未找到相关报告，请检查报告编号是否正确', 'error');
                    reportInput.focus();
                }
            });
            
            // 下载按钮点击事件
            downloadBtn.addEventListener('click', function() {
                const reportId = reportInput.value.trim();
                
                if (!reports[reportId]) {
                    showStatus('请先查询有效的报告', 'error');
                    return;
                }
                
                // 使用浏览器生成PDF
                generatePDF(reportId);
                showStatus('正在生成PDF文件...', 'success');
            });
            
            // 生成PDF函数
            function generatePDF(reportId) {
                if (!reports[reportId]) return;
                
                // 创建一个新的窗口或iframe来生成PDF内容
                const pdfWindow = window.open('', '_blank');
                
                // 根据报告ID生成不同的内容
                let content = '';
                if (reportId === 'BV2025TC106691956') {
                    content = `
                        <!DOCTYPE html>
                        <html>
                        <head>
                            <title>${reports[reportId].number}</title>
                            <style>
                                body { font-family: Arial, sans-serif; padding: 20px; line-height: 1.6; }
                                .header { text-align: center; margin-bottom: 30px; border-bottom: 2px solid #333; padding-bottom: 20px; }
                                .content { margin: 20px 0; }
                                .section { margin-bottom: 20px; }
                                .label { font-weight: bold; }
                                .footer { margin-top: 50px; text-align: center; font-size: 12px; color: #666; border-top: 1px solid #333; padding-top: 20px; }
                                table { width: 100%; border-collapse: collapse; margin: 20px 0; }
                                th, td { border: 1px solid #ddd; padding: 10px; text-align: left; }
                                th { background-color: #f2f2f2; }
                                .page-break { page-break-after: always; }
                            </style>
                        </head>
                        <body>
                            <div class="header">
                                <h1>检测报告</h1>
                                <p>报告编号: ${reports[reportId].number}</p>
                                <p>第1页共4页</p>
                            </div>
                            
                            <div class="content">
                                <div class="section">
                                    <h3>产品名称:识别卡(监督证)</h3>
                                    <h3>委托单位:河北省司法厅</h3>
                                    <h3>检验类别:委托检验</h3>
                                </div>
                                
                                <div class="section" style="text-align: center; margin-top: 50px;">
                                    <h极2>广州必维技术检测有限公司</h2>
                                    <h3>Guangzhou BV Technology Testing Co.,Ltd</h3>
                                </div>
                                
                                <div class="section" style="margin-top: 100px;">
                                    <p>地址:广州市南沙区东涌镇石排村市南公路183号东北侧首层/the first floor on the northeast side of No.183 Shinan Road, Shipai village,Dongyong Town,Nansha District,Guangzhou.</p>
                                    <p>如若对检测报告有异议，应于收到报告之日起15日内向检测单位提出，逾期不予受理。</p>
                                </div>
                            </div>
                            
                            <div class="footer">
                                <p>© 2025报告查询系统 | 本报告仅对来样负责</p>
                            </div>
                        </body>
                        </html>
                    `;
                } else {
                    content = `
                        <!DOCTYPE html>
                        <html>
                        <head>
                            <title>${reports[reportId].number}</title>
                            <style>
                                body { font-family: Arial, sans-serif; padding: 40px; }
                                .header { text-align: center; margin-bottom: 30px; }
                                .content { margin: 20px 0; }
                                .section { margin-bottom: 20px; }
                                .label { font-weight: bold; }
                                .footer { margin-top: 50px; text-align: center; font-size: 12px; color: #666; }
                            </style>
                        </head>
                        <body>
                            <div class="header">
                                <h1>检测报告</h1>
                                <p>报告编号: ${reports[reportId].number}</p>
                            </div>
                            
                            <div class="content">
                                <div class="section">
                                    <span class="label">委托单位:</span> ${reports[reportId].client}
                                </div>
                                <div class="section">
                                    <span class="label">样品名称:</span> ${reports[reportId].sample}
                                </div>
                                <div class="section">
                                    <span class="label">报告日期:</span> ${reports[reportId].date}
                                </div>
                                <div class="section">
                                    <span class="label">检测结果:</span> 样品经检测，所检项目符合要求。
                                </div>
                            </div>
                            
                            <div class="footer">
                                <p>© 2025报告查询系统 | 本报告仅对来样负责</p>
                            </div>
                        </body>
                        </html>
                    `;
                }
                
                pdfWindow.document.write(content);
                pdfWindow.document.close();
                
                // 给页面一些时间加载然后打印
                setTimeout(() => {
                    pdfWindow.print();
                }, 500);
            }
            
            // 显示状态消息
            function showStatus(message, type) {
                statusMessage.textContent = message;
                statusMessage.className = 'status-message ' + type;
                statusMessage.style.display = 'block';
            }
            
            // 按Enter键触发查询
            reportInput.addEventListener('keypress', function(e) {
                if (e.key === 'Enter') {
                    searchBtn.click();
                }
            });
        });
    </script>
</body>
</html>
