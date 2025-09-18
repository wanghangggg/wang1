<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>报告查询系统</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #1a2980, #26d0ce);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }
        
        .container {
            background-color: rgba(255, 255, 255, 0.95);
            border-radius: 15px;
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
            width: 100%;
            max-width: 900px;
            overflow: hidden;
        }
        
        .header {
            background: linear-gradient(to right, #1a2980, #26d0ce);
            color: white;
            padding: 30px 40px;
            text-align: center;
        }
        
        .header h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
            letter-spacing: 1px;
        }
        
        .header p {
            font-size: 1.1rem;
            opacity: 0.9;
        }
        
        .content {
            padding: 40px;
        }
        
        .tabs {
            display: flex;
            margin-bottom: 30px;
            border-bottom: 2px solid #eee;
        }
        
        .tab {
            padding: 15px 25px;
            font-size: 1.1rem;
            font-weight: 600;
            color: #666;
            cursor: pointer;
            transition: all 0.3s;
            border-bottom: 3px solid transparent;
        }
        
        .tab.active {
            color: #1a2980;
            border-bottom: 3px solid #1a2980;
        }
        
        .tab-content {
            display: none;
        }
        
        .tab-content.active {
            display: block;
        }
        
        .search-section, .upload-section {
            margin-bottom: 30px;
        }
        
        .input-group {
            margin-bottom: 25px;
        }
        
        .input-group label {
            display: block;
            margin-bottom: 10px;
            font-weight: 600;
            color: #333;
            font-size: 1.1rem;
        }
        
        .input-container {
            display: flex;
            width: 100%;
        }
        
        input[type="text"], input[type="file"] {
            flex: 1;
            padding: 15px 20px;
            border: 2px solid #ddd;
            border-radius: 8px;
            font-size: 1.1rem;
            transition: border-color 0.3s;
            background: white;
        }
        
        input[type="text"]:focus, input[type="file"]:focus {
            border-color: #26d0ce;
            outline: none;
            box-shadow: 0 0 0 2px rgba(38, 208, 206, 0.2);
        }
        
        button {
            background: linear-gradient(to right, #1a2980, #26d0ce);
            color: white;
            border: none;
            padding: 15px 30px;
            border-radius: 8px;
            cursor: pointer;
            font-size: 1.1rem;
            font-weight: 600;
            transition: all 0.3s;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            margin-top: 15px;
        }
        
        button:hover {
            background: linear-gradient(to right, #2234b8, #2de0de);
            transform: translateY(-2px);
        }
        
        button i {
            margin-right: 8px;
        }
        
        .example {
            background-color: #f8f9fa;
            border-left: 4px solid #26d0ce;
            padding: 15px;
            border-radius: 0 8px 8px 0;
            margin-top: 15px;
        }
        
        .example p {
            color: #666;
            font-size: 0.95rem;
        }
        
        .example strong {
            color: #1a2980;
        }
        
        .results-section {
            display: none;
            background-color: #f8f9fa;
            border-radius: 10px;
            padding: 25px;
            margin-top: 30px;
            border: 1px solid #eee;
        }
        
        .results-section h2 {
            color: #1a2980;
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 2px solid #eee;
        }
        
        .report-details {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
        }
        
        .detail-item {
            padding: 15px;
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.05);
        }
        
        .detail-item h3 {
            font-size: 0.9rem;
            color: #666;
            margin-bottom: 5px;
        }
        
        .detail-item p {
            font-size: 1.1rem;
            font-weight: 600;
            color: #333;
        }
        
        .download-section {
            margin-top: 25px;
            text-align: center;
        }
        
        .download-btn {
            background: linear-gradient(to right, #ff416c, #ff4b2b);
            color: white;
            border: none;
            padding: 15px 40px;
            border-radius: 8px;
            cursor: pointer;
            font-size: 1.1rem;
            font-weight: 600;
            transition: all 0.3s;
            display: inline-flex;
            align-items: center;
        }
        
        .download-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(255, 75, 43, 0.4);
        }
        
        .download-btn i {
            margin-right: 10px;
        }
        
        .upload-status {
            margin-top: 20px;
            padding: 15px;
            border-radius: 8px;
            display: none;
        }
        
        .upload-status.success {
            background-color: #d4edda;
            color: #155724;
            border: 1px solid #c3e6cb;
            display: block;
        }
        
        .upload-status.error {
            background-color: #f8d7da;
            color: #721c24;
            border: 1px solid #f5c6cb;
            display: block;
        }
        
        .file-input-container {
            position: relative;
            margin-bottom: 20px;
        }
        
        .file-input-label {
            display: block;
            padding: 15px 20px;
            background: #f8f9fa;
            border: 2px dashed #ddd;
            border-radius: 8px;
            text-align: center;
            cursor: pointer;
            transition: all 0.3s;
        }
        
        .file-input-label:hover {
            border-color: #26d0ce;
            background: #e6f7f7;
        }
        
        .file-input-label i {
            font-size: 2rem;
            color: #26d0ce;
            margin-bottom: 10px;
        }
        
        .file-input-label p {
            color: #666;
            margin: 5px 0;
        }
        
        input[type="file"] {
            position: absolute;
            left: 0;
            top: 0;
            opacity: 0;
            width: 100%;
            height: 100%;
            cursor: pointer;
        }
        
        .footer {
            text-align: center;
            padding: 20px;
            background-color: #f8f9fa;
            color: #666;
            font-size: 0.9rem;
            border-top: 1px solid #eee;
        }
        
        .footer a {
            color: #26d0ce;
            text-decoration: none;
        }
        
        .footer a:hover {
            text-decoration: underline;
        }
        
        @media (max-width: 600px) {
            .header {
                padding: 20px;
            }
            
            .header h1 {
                font-size: 2rem;
            }
            
            .content {
                padding: 20px;
            }
            
            .tabs {
                flex-direction: column;
            }
            
            .input-container {
                flex-direction: column;
            }
            
            input[type="text"] {
                margin-bottom: 10px;
            }
            
            button {
                width: 100%;
                padding: 15px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1><i class="fas fa-file-alt"></i> 报告查询系统</h1>
            <p>上传和查询检测报告</p>
        </div>
        
        <div class="content">
            <div class="tabs">
                <div class="tab active" data-tab="search">查询报告</div>
                <div class="tab" data-tab="upload">上传报告</div>
            </div>
            
            <div class="tab-content active" id="search-tab">
                <div class="search-section">
                    <div class="input-group">
                        <label for="report-number">报告编号</label>
                        <div class="input-container">
                            <input type="text" id="report-number" placeholder="请输入报告编号..." autocomplete="off">
                        </div>
                    </div>
                    
                    <button id="search-btn"><i class="fas fa-search"></i> 查询报告</button>
                    
                    <div class="example">
                        <p>示例报告编号：<strong>BV2025TC106691805</strong>, REP-20230915-001, REP-20230918-045, REP-20230919-112</p>
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
                </div>
            </div>
            
            <div class="tab-content" id="upload-tab">
                <div class="upload-section">
                    <h2><i class="fas fa-cloud-upload-alt"></i> 上传PDF报告</h2>
                    
                    <div class="file-input-container">
                        <label class="file-input-label">
                            <i class="fas fa-file-pdf"></i>
                            <h3>点击选择PDF文件或拖拽文件到此处</h3>
                            <p>最大文件大小: 10MB</p>
                            <p id="selected-file">未选择文件</p>
                        </label>
                        <input type="file" id="pdf-file" accept=".pdf">
                    </div>
                    
                    <div class="input-group">
                        <label for="report-id">报告编号</label>
                        <input type="text" id="report-id" placeholder="输入报告编号...">
                    </div>
                    
                    <button id="upload-btn"><i class="fas fa-upload"></i> 上传报告</button>
                    
                    <div class="upload-status" id="upload-status"></div>
                </div>
            </div>
        </div>
        
        <div class="footer">
            <p>© 2025报告查询系统 | 技术支持: <a href="#">400-888-9999</a></p>
        </div>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            // 选项卡切换
            const tabs = document.querySelectorAll('.tab');
            const tabContents = document.querySelectorAll('.tab-content');
            
            tabs.forEach(tab => {
                tab.addEventListener('click', () => {
                    const tabId = tab.getAttribute('data-tab');
                    
                    // 更新选项卡状态
                    tabs.forEach(t => t.classList.remove('active'));
                    tab.classList.add('active');
                    
                    // 更新内容显示
                    tabContents.forEach(content => {
                        content.classList.remove('active');
                        if (content.id === `${tabId}-tab`) {
                            content.classList.add('active');
                        }
                    });
                });
            });
            
            // 查询功能
            const searchBtn = document.getElementById('search-btn');
            const reportInput = document.getElementById('report-number');
            const resultsSection = document.getElementById('results');
            const downloadBtn = document.getElementById('download-btn');
            
            // 报告数据
            const reports = {
                'BV2025TC106691805': {
                    number: 'BV2025TC106691805',
                    client: '河北省司法厅',
                    sample: '国徽（行政执法、监督证）',
                    date: '2025年09月18日',
                    pdf: '国徽-行政执法、监督证.pdf'
                }
            };
            
            // 查询按钮点击事件
            searchBtn.addEventListener('click', function() {
                const reportId = reportInput.value.trim();
                
                if (!reportId) {
                    alert('请输入报告编号');
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
                } else {
                    alert('未找到相关报告，请检查报告编号是否正确');
                    reportInput.focus();
                }
            });
            
            // 下载按钮点击事件
            downloadBtn.addEventListener('click', function() {
                const reportId = reportInput.value.trim();
                if (reports[reportId]) {
                    // 创建临时链接下载PDF
                    const link = document.createElement('a');
                    link.href = reports[reportId].pdf;
                    link.download = reports[reportId].pdf;
                    document.body.appendChild(link);
                    link.click();
                    document.body.removeChild(link);
                }
            });
            
            // 按Enter键触发查询
            reportInput.addEventListener('keypress', function(e) {
                if (e.key === 'Enter') {
                    searchBtn.click();
                }
            });
            
            // 上传功能
            const pdfFileInput = document.getElementById('pdf-file');
            const reportIdInput = document.getElementById('report-id');
            const uploadBtn = document.getElementById('upload-btn');
            const uploadStatus = document.getElementById('upload-status');
            const selectedFile = document.getElementById('selected-file');
            
            // 文件选择事件
            pdfFileInput.addEventListener('change', function() {
                if (this.files.length > 0) {
                    selectedFile.textContent = `已选择: ${this.files[0].name}`;
                } else {
                    selectedFile.textContent = '未选择文件';
                }
            });
            
            // 上传按钮点击事件
            uploadBtn.addEventListener('click', function() {
                const file = pdfFileInput.files[0];
                const reportId = reportIdInput.value.trim();
                
                if (!file) {
                    showUploadStatus('请选择PDF文件', 'error');
                    return;
                }
                
                if (!reportId) {
                    showUploadStatus('请输入报告编号', 'error');
                    reportIdInput.focus();
                    return;
                }
                
                if (file.type !== 'application/pdf') {
                    showUploadStatus('请选择PDF格式的文件', 'error');
                    return;
                }
                
                if (file.size > 10 * 1024 * 1024) {
                    showUploadStatus('文件大小不能超过10MB', 'error');
                    return;
                }
                
                // 模拟上传过程
                showUploadStatus('文件上传中...', '');
                
                setTimeout(() => {
                    // 模拟上传成功
                    showUploadStatus(`报告 "${file.name}" 上传成功！报告编号: ${reportId}`, 'success');
                    
                    // 添加到报告列表
                    reports[reportId] = {
                        number: reportId,
                        client: '上传用户',
                        sample: '自定义样品',
                        date: new Date().toLocaleDateString(),
                        pdf: URL.createObjectURL(file)
                    };
                    
                    // 清空表单
                    pdfFileInput.value = '';
                    reportIdInput.value = '';
                    selectedFile.textContent = '未选择文件';
                }, 2000);
            });
            
            // 显示上传状态
            function showUploadStatus(message, type) {
                uploadStatus.textContent = message;
                uploadStatus.className = 'upload-status';
                
                if (type) {
                    uploadStatus.classList.add(type);
                }
            }
            
            // 拖拽上传功能
            const fileInputLabel = document.querySelector('.file-input-label');
            
            fileInputLabel.addEventListener('dragover', function(e) {
                e.preventDefault();
                this.style.borderColor = '#26d0ce';
                this.style.backgroundColor = '#e6f7f7';
            });
            
            fileInputLabel.addEventListener('dragleave', function() {
                this.style.borderColor = '#ddd';
                this.style.backgroundColor = '#f8f9fa';
            });
            
            fileInputLabel.addEventListener('drop', function(e) {
                e.preventDefault();
                this.style.borderColor = '#ddd';
                this.style.backgroundColor = '#f8f9fa';
                
                if (e.dataTransfer.files.length > 0) {
                    pdfFileInput.files = e.dataTransfer.files;
                    selectedFile.textContent = `已选择: ${e.dataTransfer.files[0].name}`;
                }
            });
        });
    </script>
</body>
</html>
