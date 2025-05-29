<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DeepSeek R1：认识身边的智能助手</title>
    
    <!-- Reveal.js -->
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/reveal.js@4.3.1/dist/reveal.css">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/reveal.js@4.3.1/dist/theme/black.css">
    
    <!-- Font Awesome -->
    <link rel="stylesheet" href="https://cdn.staticfile.org/font-awesome/6.4.0/css/all.min.css">
    
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Noto+Serif+SC:wght@400;500;600;700&family=Noto+Sans+SC:wght@300;400;500;700&display=swap" rel="stylesheet">
    
    <style>
        :root {
            --primary: #6a11cb;
            --secondary: #2575fc;
            --accent: #00c9ff;
            --light: #f8f9fa;
            --dark: #212529;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Noto Sans SC', Tahoma, Arial, Roboto, "Droid Sans", "Helvetica Neue", "Droid Sans Fallback", "Heiti SC", "Hiragino Sans GB", Simsun, sans-serif;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: var(--light);
            overflow: hidden;
        }
        
        .reveal {
            background: linear-gradient(135deg, #0f0c29, #302b63, #24243e);
            color: var(--light);
        }
        
        .reveal-viewport {
            background: rgba(0, 0, 0, 0.7);
        }
        
        .reveal .slides {
            text-align: left;
            font-family: 'Noto Sans SC', sans-serif;
        }
        
        /* 标题样式 */
        .reveal h1, 
        .reveal h2, 
        .reveal h3, 
        .reveal h4, 
        .reveal h5 {
            font-family: 'Noto Serif SC', serif;
            font-weight: 700;
            color: var(--light);
            text-shadow: 0 2px 10px rgba(0,0,0,0.3);
            margin-bottom: 1rem;
        }
        
        .reveal h1 {
            font-size: 3.5rem;
            line-height: 1.2;
            background: linear-gradient(to right, var(--accent), #ffffff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 1.5rem;
        }
        
        .reveal h2 {
            font-size: 2.5rem;
            border-left: 5px solid var(--accent);
            padding-left: 1rem;
            margin-bottom: 1.5rem;
        }
        
        .reveal h3 {
            font-size: 2rem;
            color: var(--accent);
            margin-bottom: 1rem;
        }
        
        /* 段落样式 */
        .reveal p {
            font-size: 1.5rem;
            line-height: 1.6;
            margin-bottom: 1.2rem;
            max-width: 90%;
        }
        
        .reveal li {
            font-size: 1.4rem;
            line-height: 1.6;
            margin-bottom: 0.8rem;
        }
        
        /* 内容容器 */
        .content-box {
            background: rgba(255, 255, 255, 0.08);
            backdrop-filter: blur(10px);
            border-radius: 15px;
            padding: 2rem;
            margin: 1.5rem 0;
            border: 1px solid rgba(255, 255, 255, 0.1);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        }
        
        /* 图标样式 */
        .icon-box {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 60px;
            height: 60px;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            border-radius: 50%;
            margin-right: 1rem;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }
        
        .icon-box i {
            font-size: 1.8rem;
            color: white;
        }
        
        /* 列表样式 */
        .feature-list li {
            display: flex;
            align-items: flex-start;
            margin-bottom: 1.5rem;
        }
        
        /* 封面页样式 */
        .title-slide {
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            height: 100%;
            background: linear-gradient(135deg, rgba(106, 17, 203, 0.8), rgba(37, 117, 252, 0.8));
            border-radius: 20px;
            padding: 4rem;
        }
        
        .title-slide h1 {
            font-size: 4.5rem;
            margin-bottom: 1rem;
            text-shadow: 0 5px 15px rgba(0,0,0,0.4);
        }
        
        .title-slide h2 {
            font-size: 2.2rem;
            font-weight: 400;
            border: none;
            padding: 0;
            margin-bottom: 3rem;
            color: rgba(255, 255, 255, 0.9);
        }
        
        .title-slide .subtitle {
            font-size: 1.8rem;
            margin-top: 2rem;
            color: var(--accent);
        }
        
        .logo {
            width: 200px;
            height: 200px;
            background: linear-gradient(135deg, var(--accent), #ffffff);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 2rem auto;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        }
        
        .logo i {
            font-size: 6rem;
            color: var(--dark);
        }
        
        /* 时间线样式 */
        .timeline {
            position: relative;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .timeline::after {
            content: '';
            position: absolute;
            width: 6px;
            background: linear-gradient(to bottom, var(--primary), var(--accent));
            top: 0;
            bottom: 0;
            left: 50%;
            margin-left: -3px;
            border-radius: 3px;
        }
        
        .timeline-item {
            padding: 10px 40px;
            position: relative;
            width: 50%;
            box-sizing: border-box;
        }
        
        .timeline-item:nth-child(odd) {
            left: 0;
        }
        
        .timeline-item:nth-child(even) {
            left: 50%;
        }
        
        .timeline-content {
            padding: 20px 30px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 10px;
            border-left: 4px solid var(--accent);
        }
        
        .timeline-item::after {
            content: '';
            position: absolute;
            width: 20px;
            height: 20px;
            background: var(--accent);
            border: 4px solid var(--primary);
            top: 20px;
            border-radius: 50%;
            z-index: 1;
        }
        
        .timeline-item:nth-child(odd)::after {
            right: -12px;
        }
        
        .timeline-item:nth-child(even)::after {
            left: -12px;
        }
        
        /* 对比表格样式 */
        .comparison-table {
            width: 100%;
            border-collapse: collapse;
            margin: 2rem 0;
            font-size: 1.3rem;
        }
        
        .comparison-table th {
            background: linear-gradient(to right, var(--primary), var(--secondary));
            color: white;
            padding: 15px;
            text-align: left;
        }
        
        .comparison-table td {
            padding: 12px 15px;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .comparison-table tr:nth-child(even) {
            background: rgba(255, 255, 255, 0.05);
        }
        
        /* 步骤演示样式 */
        .step-container {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            margin: 2rem 0;
        }
        
        .step {
            flex: 1;
            min-width: 300px;
            background: rgba(255, 255, 255, 0.08);
            border-radius: 10px;
            padding: 20px;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .step-number {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background: var(--accent);
            color: var(--dark);
            border-radius: 50%;
            font-weight: bold;
            margin-bottom: 15px;
        }
        
        /* 响应式调整 */
        @media (max-width: 768px) {
            .reveal h1 {
                font-size: 2.5rem;
            }
            
            .reveal h2 {
                font-size: 2rem;
            }
            
            .reveal p, .reveal li {
                font-size: 1.2rem;
            }
            
            .title-slide h1 {
                font-size: 3rem;
            }
            
            .timeline::after {
                left: 31px;
            }
            
            .timeline-item {
                width: 100%;
                padding-left: 70px;
                padding-right: 25px;
            }
            
            .timeline-item:nth-child(even) {
                left: 0;
            }
            
            .timeline-item::after {
                left: 21px;
            }
        }
        
        /* 特殊幻灯片样式 */
        .quote-slide {
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            height: 100%;
        }
        
        .quote {
            font-size: 2.5rem;
            font-style: italic;
            max-width: 90%;
            line-height: 1.6;
            position: relative;
            padding: 0 2rem;
        }
        
        .quote::before, .quote::after {
            content: '"';
            font-size: 4rem;
            color: var(--accent);
            position: absolute;
        }
        
        .quote::before {
            top: -1.5rem;
            left: -1rem;
        }
        
        .quote::after {
            bottom: -3rem;
            right: -1rem;
        }
        
        .source {
            font-size: 1.5rem;
            margin-top: 3rem;
            color: rgba(255, 255, 255, 0.7);
        }
        
        /* 按钮样式 */
        .action-button {
            display: inline-block;
            background: linear-gradient(to right, var(--accent), #00ffea);
            color: var(--dark);
            padding: 12px 30px;
            border-radius: 50px;
            font-weight: bold;
            text-decoration: none;
            margin-top: 1.5rem;
            font-size: 1.3rem;
            border: none;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }
        
        .action-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.3);
        }
        
        /* 练习卡片 */
        .exercise-card {
            background: rgba(255, 255, 255, 0.1);
            border-radius: 15px;
            padding: 2rem;
            margin: 1.5rem 0;
            border-left: 5px solid var(--accent);
        }
        
        .exercise-card h4 {
            color: var(--accent);
            margin-bottom: 1rem;
        }
        
        /* 结束页 */
        .end-slide {
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            height: 100%;
        }
        
        .end-slide h1 {
            margin-bottom: 2rem;
        }
        
        .contact-info {
            display: flex;
            gap: 2rem;
            margin-top: 2rem;
        }
        
        .contact-item {
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        
        .contact-icon {
            font-size: 2.5rem;
            color: var(--accent);
            margin-bottom: 1rem;
        }
    </style>
</head>
<body>
    <div class="reveal">
        <div class="slides">
            <!-- 封面页 -->
            <section>
                <div class="title-slide">
                    <div class="logo">
                        <i class="fas fa-brain"></i>
                    </div>
                    <h1>DeepSeek R1</h1>
                    <h2>认识身边的智能助手</h2>
                    <p>生成式AI革命与智能助手应用</p>
                    <p class="subtitle">开启AI赋能的新时代</p>
                </div>
            </section>
            
            <!-- AI 介绍 -->
            <section>
                <section>
                    <h2>AI是什么？</h2>
                    <div class="content-box">
                        <p>人工智能(AI)是通过算法和数据，让机器能学习、能推理、能模仿人的智能行为的技术。</p>
                        <p><strong>说人话：</strong>AI是让机器像人一样思考、行动的技术。</p>
                        <div class="fragment">
                            <div class="icon-box">
                                <i class="fas fa-robot"></i>
                            </div>
                            <h3>AI的核心能力</h3>
                            <ul>
                                <li>自然语言处理（听懂你的话）</li>
                                <li>计算机视觉（看懂图片）</li>
                                <li>自主决策（自己做决定）</li>
                            </ul>
                        </div>
                    </div>
                </section>
                
                <section>
                    <h2>AI的核心本质</h2>
                    <div class="content-box">
                        <div class="quote">
                            记住：AI的核心就是学习和模仿
                        </div>
                        <div class="fragment">
                            <h3>实际应用示例</h3>
                            <p>短视频平台通过AI分析你的喜好，不断推荐相关内容</p>
                            <p>背后是大量、重复的数据训练</p>
                        </div>
                    </div>
                </section>
            </section>
            
            <!-- AI发展史 -->
            <section>
                <h2>AI进化史</h2>
                <p>从达特茅斯会议到DeepSeek的狂飙时代</p>
                
                <div class="timeline">
                    <div class="timeline-item">
                        <div class="timeline-content">
                            <h3>缘起期 (1950-1956)</h3>
                            <ul>
                                <li>1950年：马文·明斯基建造全球第一台神经网络计算机</li>
                                <li>阿兰·图灵提出图灵测试</li>
                                <li>1956年：达特茅斯会议首次提出"人工智能"概念</li>
                            </ul>
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-content">
                            <h3>萌芽期 (1986)</h3>
                            <p>杰弗里·辛顿提出AI应模仿人类大脑神经网络</p>
                            <p>开创"深度学习"道路</p>
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-content">
                            <h3>探索沉淀期 (2010左右)</h3>
                            <ul>
                                <li>Google推出AlphaGo</li>
                                <li>2012年：语音和图像识别突破</li>
                                <li>2014年：微软推出小冰聊天机器人</li>
                            </ul>
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-content">
                            <h3>迅猛发展期 (2022至今)</h3>
                            <ul>
                                <li>2022年底：ChatGPT 3.5横空出世</li>
                                <li>2025年1月：DeepSeek R1面世</li>
                                <li>2025年2-3月：Claude 3.7、Gemini 2.0、GPT-4o相继升级</li>
                            </ul>
                        </div>
                    </div>
                </div>
            </section>
            
            <!-- AI现状洞察 -->
            <section>
                <div class="quote-slide">
                    <div class="quote">
                        了解AI的发展历史，不是为了记年份，而是要抓住核心：AI像人，但它不是人
                    </div>
                    <p class="source">现阶段，AI是一个强大的工具</p>
                </div>
            </section>
            
            <!-- DeepSeek介绍 -->
            <section>
                <section>
                    <h2>认识DeepSeek</h2>
                    <div class="content-box">
                        <p>由杭州"深度求索"公司开发的大语言模型智能助手</p>
                        <p class="fragment">定位：<strong>中文语境下的推理之王</strong></p>
                        <div class="fragment">
                            <h3>核心能力</h3>
                            <ul class="feature-list">
                                <li>
                                    <div class="icon-box">
                                        <i class="fas fa-briefcase"></i>
                                    </div>
                                    <span>职场赋能：解答疑问、激发创意</span>
                                </li>
                                <li>
                                    <div class="icon-box">
                                        <i class="fas fa-graduation-cap"></i>
                                    </div>
                                    <span>学习支持：解决学习痛点</span>
                                </li>
                                <li>
                                    <div class="icon-box">
                                        <i class="fas fa-home"></i>
                                    </div>
                                    <span>生活助手：沟通技巧、美食菜谱等</span>
                                </li>
                            </ul>
                        </div>
                    </div>
                </section>
                
                <section>
                    <h2>推理模型 vs 基础通用模型</h2>
                    <table class="comparison-table">
                        <tr>
                            <th>对比维度</th>
                            <th>基础通用模型</th>
                            <th>推理模型</th>
                        </tr>
                        <tr>
                            <td>核心能力</td>
                            <td>广泛适用性（文本生成、翻译等）</td>
                            <td>专注逻辑推理（报告分析、代码纠错等）</td>
                        </tr>
                        <tr>
                            <td>训练模式</td>
                            <td>预训练和监督微调</td>
                            <td>强化学习训练</td>
                        </tr>
                        <tr>
                            <td>典型代表</td>
                            <td>ChatGPT4o、Claude2.5、豆包</td>
                            <td>DeepSeek R1、Gemini2.5Pro</td>
                        </tr>
                        <tr>
                            <td>擅长任务</td>
                            <td>通用场景</td>
                            <td>实时决策、复杂推理</td>
                        </tr>
                        <tr>
                            <td>性能短板</td>
                            <td>存在AI幻觉</td>
                            <td>响应速度慢，存在AI幻觉</td>
                        </tr>
                    </table>
                </section>
                
                <section>
                    <h2>模型使用对比示例</h2>
                    <div class="step-container">
                        <div class="step">
                            <div class="step-number">1</div>
                            <h3>通用模型 (ChatGPT-4o)</h3>
                            <p>需要多步骤操作：</p>
                            <ol>
                                <li>设定角色</li>
                                <li>上传资料</li>
                                <li>确认理解</li>
                                <li>提出需求</li>
                            </ol>
                        </div>
                        <div class="step">
                            <div class="step-number">2</div>
                            <h3>推理模型 (DeepSeek R1)</h3>
                            <p>一步到位操作：</p>
                            <ol>
                                <li>直接提出需求</li>
                                <li>获得完整答案</li>
                            </ol>
                        </div>
                    </div>
                </section>
            </section>
            
            <!-- DeepSeek核心优势 -->
            <section>
                <h2>DeepSeek的五大核心优势</h2>
                <div class="content-box">
                    <ul class="feature-list">
                        <li>
                            <div class="icon-box" style="background: linear-gradient(135deg, #ff6b6b, #ff8e53);">
                                <i class="fas fa-language"></i>
                            </div>
                            <div>
                                <h3>更懂中文</h3>
                                <p>深入理解中文成语、诗词和网络热梗，符合国人表达习惯</p>
                            </div>
                        </li>
                        <li>
                            <div class="icon-box" style="background: linear-gradient(135deg, #4facfe, #00f2fe);">
                                <i class="fas fa-brain"></i>
                            </div>
                            <div>
                                <h3>推理能力强，持续进化</h3>
                                <p>擅长逻辑推理，通过用户反馈不断学习进化</p>
                            </div>
                        </li>
                        <li>
                            <div class="icon-box" style="background: linear-gradient(135deg, #42e695, #3bb2b8);">
                                <i class="fas fa-comments"></i>
                            </div>
                            <div>
                                <h3>输出能力强</h3>
                                <p>上下文理解优秀，多轮对话不跑题，自然延伸话题</p>
                            </div>
                        </li>
                        <li>
                            <div class="icon-box" style="background: linear-gradient(135deg, #ff9a9e, #fad0c4);">
                                <i class="fas fa-shield-alt"></i>
                            </div>
                            <div>
                                <h3>安全可靠</h3>
                                <p>敏感信息过滤，自动熔断不当内容</p>
                            </div>
                        </li>
                        <li>
                            <div class="icon-box" style="background: linear-gradient(135deg, #a18cd1, #fbc2eb);">
                                <i class="fas fa-globe-asia"></i>
                            </div>
                            <div>
                                <h3>多语言翻译</h3>
                                <p>支持全球主流语言高质量翻译</p>
                            </div>
                        </li>
                    </ul>
                </div>
            </section>
            
            <!-- 实操案例 -->
            <section>
                <section>
                    <h2>实操分享：告别熬夜加班</h2>
                    <p>让AI成为工作效率倍增器</p>
                    <div class="step-container">
                        <div class="step">
                            <div class="step-number">1</div>
                            <h3>DeepSeek + 讯飞智文</h3>
                            <p>一键生成精美PPT</p>
                        </div>
                        <div class="step">
                            <div class="step-number">2</div>
                            <h3>DeepSeek + Word</h3>
                            <p>60秒搞定文档排版</p>
                        </div>
                        <div class="step">
                            <div class="step-number">3</div>
                            <h3>DeepSeek + Excel</h3>
                            <p>文本秒变数据表格</p>
                        </div>
                    </div>
                </section>
                
                <section>
                    <h3>案例一：PPT智能生成</h3>
                    <div class="content-box">
                        <ol>
                            <li>在DeepSeek输入PPT制作要求</li>
                            <li>获取生成的文案内容</li>
                            <li>打开讯飞智文平台 (https://zhiwen.xfyun.cn/)</li>
                            <li>粘贴文案并选择模板</li>
                            <li>一键生成精美PPT</li>
                        </ol>
                        <p class="fragment" style="color: #ff6b6b; margin-top: 1.5rem;">
                            <i class="fas fa-exclamation-triangle"></i> 重要提示：一定要检查内容准确性
                        </p>
                    </div>
                </section>
                
                <section>
                    <h3>案例二：Word文档排版</h3>
                    <div class="content-box">
                        <ol>
                            <li>向DeepSeek提出文档需求</li>
                            <li>获取生成的文档内容</li>
                            <li>复制到Word文档中</li>
                            <li>应用DeepSeek建议的样式</li>
                            <li>60秒完成专业排版</li>
                        </ol>
                        <p class="fragment" style="color: #ff6b6b; margin-top: 1.5rem;">
                            <i class="fas fa-exclamation-triangle"></i> 重要提示：AI也会"摸鱼划水"，需认真检查
                        </p>
                    </div>
                </section>
                
                <section>
                    <h3>案例三：Excel表格生成</h3>
                    <div class="content-box">
                        <ol>
                            <li>向DeepSeek提供文本数据</li>
                            <li>指定需要的表格格式</li>
                            <li>获取生成的表格结构</li>
                            <li>复制到Excel中</li>
                            <li>一键完成数据整理</li>
                        </ol>
                        <p class="fragment" style="color: #ff6b6b; margin-top: 1.5rem;">
                            <i class="fas fa-exclamation-triangle"></i> 重要提示：AI不会主动核对数据准确性
                        </p>
                    </div>
                </section>
            </section>
            
            <!-- 快速上手指南 -->
            <section>
                <h2>DeepSeek快速上手指南</h2>
                <div class="content-box">
                    <div class="step-container">
                        <div class="step">
                            <div class="step-number">1</div>
                            <h3>PC网页版</h3>
                            <ol>
                                <li>访问 https://www.deepseek.com/</li>
                                <li>点击"开始对话"</li>
                                <li>注册并登录账号</li>
                            </ol>
                        </div>
                        <div class="step">
                            <div class="step-number">2</div>
                            <h3>手机APP版</h3>
                            <ol>
                                <li>应用商店搜索"DeepSeek"</li>
                                <li>认准"杭州深度求索"公司</li>
                                <li>下载安装并登录</li>
                            </ol>
                        </div>
                    </div>
                    <div class="fragment">
                        <p style="margin-top: 2rem;">
                            <i class="fas fa-info-circle"></i> 当官方产品繁忙时，可使用替代应用：
                            问小白、腾讯元宝等
                        </p>
                    </div>
                </div>
            </section>
            
            <!-- 课后练习 -->
            <section>
                <h2>课后练习</h2>
                <div class="content-box">
                    <p>请任选一个实操案例完成练习：</p>
                    
                    <div class="exercise-card">
                        <h4>选项一：PPT制作</h4>
                        <p>用DeepSeek+讯飞智文制作关于「市民夜校」社区推广的PPT (10页)</p>
                    </div>
                    
                    <div class="exercise-card">
                        <h4>选项二：Word文档</h4>
                        <p>用DeepSeek+Word撰写"如何保持健康生活习惯"短文并进行排版</p>
                    </div>
                    
                    <div class="exercise-card">
                        <h4>选项三：Excel表格</h4>
                        <p>用DeepSeek+Excel整理你感兴趣领域的知识获取成长计划</p>
                    </div>
                    
                    <div class="fragment">
                        <h3 style="margin-top: 2rem;">提交要求</h3>
                        <ul>
                            <li>时间：本周六（4月19日）中午12点前</li>
                            <li>方式：上传电子文档到学习群</li>
                            <li>命名格式：区域+姓名+题目+日期 (例：江湾+张三+DS与PPT练习+0419)</li>
                        </ul>
                    </div>
                </div>
            </section>
            
            <!-- 结束页 -->
            <section>
                <div class="end-slide">
                    <h1>开启你的AI之旅</h1>
                    <p>让DeepSeek成为你的智能助手</p>
                    <a href="https://www.deepseek.com" class="action-button">
                        <i class="fas fa-rocket"></i> 立即体验DeepSeek
                    </a>
                    
                    <div class="contact-info">
                        <div class="contact-item">
                            <div class="contact-icon">
                                <i class="fab fa-weixin"></i>
                            </div>
                            <span>学习群：AI助手交流</span>
                        </div>
                        <div class="contact-item">
                            <div class="contact-icon">
                                <i class="fas fa-envelope"></i>
                            </div>
                            <span>contact@deepseek.com</span>
                        </div>
                        <div class="contact-item">
                            <div class="contact-icon">
                                <i class="fas fa-globe"></i>
                            </div>
                            <span>www.deepseek.com</span>
                        </div>
                    </div>
                </div>
            </section>
        </div>
    </div>

    <script src="https://cdn.jsdelivr.net/npm/reveal.js@4.3.1/dist/reveal.js"></script>
    <script>
        Reveal.initialize({
            controls: true,
            progress: true,
            center: true,
            hash: true,
            transition: 'slide',
            backgroundTransition: 'fade',
            pdfSeparateFragments: false,
            
            // 响应式调整
            width: '100%',
            height: '100%',
            margin: 0.08,
            minScale: 0.2,
            maxScale: 2.0,
            
            // 插件
            plugins: []
        });
        
        // 添加键盘快捷键说明
        document.addEventListener('keydown', function(event) {
            if(event.key === '?') {
                alert([
                    '导航快捷键:',
                    '- 空格键: 下一张幻灯片',
                    '- 方向键: 导航幻灯片',
                    '- ESC: 幻灯片概览',
                    '- B: 黑屏暂停',
                    '- F: 全屏切换'
                ].join('\n'));
            }
        }, false);
    </script>
</body>
</html>
