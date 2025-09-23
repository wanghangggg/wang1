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
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
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
            box-shadow: inset 0 0 0 2px #26d0ce;
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
            }
            
            input[type="text"] {
                border-radius: 8px;
                margin-bottom: 10px;
            }
            
            button {
                border-radius: 8px;
                padding: 15px;
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
                    <label for="report-number">报告编号</label>
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
                        <i class="fas fa-download"></i> 下载完整报告 (PDF)
                    </button>
                </div>
                
                <div class="status-message" id="status-message"></div>
            </div>
        </div>
        
        <div class="footer">
            <p>© 2025 报告查询系统 | 专业技术检测服务</p>
        </div>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const searchBtn = document.getElementById('search-btn');
            const reportInput = document.getElementById('report-number');
            const resultsSection = document.getElementById('results');
            const downloadBtn = document.getElementById('download-btn');
            const statusMessage = document.getElementById('status-message');
            
            // 报告数据 - 根据提供的PDF文档信息更新
            const reports = {
                'BV2025TC106691805': {
                    number: 'BV2025TC106691805',
                    client: '河北省司法厅',
                    sample: '执法证、监督证-国徽颜色',
                    date: '2025年09月18日',
                    pdf: '执法证、监督证-国徽颜色.pdf'
                },
                'BV2025TC106691956': {
                    number: 'BV2025TC106691956',
                    client: '河北省司法厅',
                    sample: '执法证-识别卡',
                    date: '2025年09月22日',
                    pdf: '执法证-识别卡.pdf'
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
                    
                    showStatus('找到报告，点击下载按钮获取PDF文件', 'success');
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
                
                // 从服务器下载PDF
                const pdfUrl = reports[reportId].pdf;
                
                // 创建临时链接下载PDF
                const link = document.createElement('a');
                link.href = pdfUrl;
                link.download = reports[reportId].pdf;
                link.target = '_blank'; // 在新标签页打开
                document.body.appendChild(link);
                
                // 模拟点击
                link.click();
                
                // 移除链接
                document.body.removeChild(link);
                
                showStatus('正在下载PDF文件...', 'success');
            });
            
            // 显示状态消息
            function showStatus(message, type) {
                statusMessage.textContent = message;
                statusMessage.className = 'status-message ' + type;
                statusMessage.style.display = 'block';
                
                // 5秒后自动隐藏消息
                setTimeout(() => {
                    statusMessage.style.display = 'none';
                }, 5000);
            }
            });
        });
    </script>
</body>
</html>
