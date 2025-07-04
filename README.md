# dsi
dsi
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Путь к стройности: эффективные методы похудения</title>
    <style>
        :root {
            --primary: #4CAF50;
            --secondary: #8BC34A;
            --accent: #FFC107;
            --light: #F1F8E9;
            --dark: #2E7D32;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            margin: 0;
            padding: 0;
            background-color: var(--light);
            color: #333;
            line-height: 1.6;
        }
        
        header {
            background: linear-gradient(135deg, var(--primary), var(--dark));
            color: white;
            padding: 2rem 0;
            text-align: center;
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
        }
        
        nav {
            background-color: white;
            padding: 1rem;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        nav ul {
            display: flex;
            justify-content: center;
            list-style: none;
            padding: 0;
            margin: 0;
            flex-wrap: wrap;
        }
        
        nav li {
            margin: 0 1rem;
        }
        
        nav a {
            text-decoration: none;
            color: var(--dark);
            font-weight: 600;
            padding: 0.5rem 1rem;
            border-radius: 20px;
            transition: all 0.3s;
        }
        
        nav a:hover {
            background-color: var(--secondary);
            color: white;
        }
        
        .container {
            max-width: 1200px;
            margin: 2rem auto;
            padding: 0 1rem;
        }
        
        .hero {
            background: url('https://images.unsplash.com/photo-1535914254981-b5012eebbd15?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80') center/cover;
            height: 400px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            text-align: center;
            position: relative;
            margin-bottom: 2rem;
            border-radius: 8px;
            overflow: hidden;
        }
        
        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.5);
        }
        
        .hero-content {
            position: relative;
            z-index: 1;
            padding: 2rem;
            max-width: 800px;
        }
        
        .method-card {
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            margin-bottom: 2rem;
            overflow: hidden;
            transition: transform 0.3s;
        }
        
        .method-card:hover {
            transform: translateY(-5px);
        }
        
        .method-header {
            background-color: var(--primary);
            color: white;
            padding: 1rem;
            cursor: pointer;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .method-content {
            padding: 0 1.5rem;
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.3s ease-out, padding 0.3s ease;
        }
        
        .method-content.active {
            padding: 1.5rem;
            max-height: 5000px;
        }
        
        .exercise {
            margin-bottom: 1.5rem;
            padding-bottom: 1.5rem;
            border-bottom: 1px solid #eee;
        }
        
        .exercise:last-child {
            border-bottom: none;
        }
        
        .difficulty-tabs {
            display: flex;
            margin-bottom: 1rem;
            border-bottom: 2px solid #eee;
            flex-wrap: wrap;
        }
        
        .difficulty-tab {
            padding: 0.5rem 1rem;
            cursor: pointer;
            margin-right: 0.5rem;
            border-radius: 4px 4px 0 0;
            transition: all 0.3s;
        }
        
        .difficulty-tab:hover {
            background-color: var(--light);
        }
        
        .difficulty-tab.active {
            background-color: var(--primary);
            color: white;
        }
        
        .difficulty-content {
            display: none;
        }
        
        .difficulty-content.active {
            display: block;
        }
        
        .video-link {
            display: inline-block;
            margin-top: 0.5rem;
            color: var(--dark);
            text-decoration: none;
            font-weight: 600;
            background-color: var(--light);
            padding: 0.3rem 0.8rem;
            border-radius: 4px;
            transition: all 0.3s;
        }
        
        .video-link:hover {
            background-color: var(--accent);
            text-decoration: none;
        }
        
        .video-link::before {
            content: "▶";
            margin-right: 5px;
        }
        
        .duration {
            display: inline-block;
            background-color: var(--accent);
            color: #333;
            padding: 0.2rem 0.5rem;
            border-radius: 4px;
            font-size: 0.8rem;
            margin-left: 0.5rem;
            font-weight: bold;
        }
        
        .method-icon {
            font-size: 1.2rem;
            transition: transform 0.3s;
        }
        
        .method-header.active .method-icon {
            transform: rotate(180deg);
        }
        
        footer {
            background-color: var(--dark);
            color: white;
            text-align: center;
            padding: 2rem 0;
            margin-top: 2rem;
        }
        
        .progress-section {
            background-color: white;
            padding: 2rem;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            margin-bottom: 2rem;
        }
        
        .progress-form {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 1rem;
        }
        
        .form-group {
            margin-bottom: 1rem;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 600;
        }
        
        .form-group input, .form-group select {
            width: 100%;
            padding: 0.5rem;
            border: 1px solid #ddd;
            border-radius: 4px;
        }
        
        button {
            background-color: var(--primary);
            color: white;
            border: none;
            padding: 0.7rem 1.5rem;
            border-radius: 4px;
            cursor: pointer;
            font-weight: 600;
            transition: background-color 0.3s;
        }
        
        button:hover {
            background-color: var(--dark);
        }
        
        .nutrition-tips {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 1.5rem;
            margin-top: 2rem;
        }
        
        .tip-card {
            background-color: white;
            border-radius: 8px;
            padding: 1.5rem;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }
        
        @media (max-width: 768px) {
            nav ul {
                flex-direction: column;
                align-items: center;
            }
            
            nav li {
                margin: 0.5rem 0;
            }
            
            .hero {
                height: 300px;
            }
            
            .progress-form {
                grid-template-columns: 1fr;
            }
            
            .nutrition-tips {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>Путь к стройности</h1>
        <p>Эффективные методы похудения для каждого</p>
    </header>
    
    <nav>
        <ul>
            <li><a href="#home">Главная</a></li>
            <li><a href="#methods">Методы</a></li>
            <li><a href="#difficulty">По сложности</a></li>
            <li><a href="#nutrition">Питание</a></li>
            <li><a href="#progress">Отслеживание</a></li>
        </ul>
    </nav>
    
    <div class="container">
        <section id="home" class="hero">
            <div class="hero-content">
                <h2>Начните свой путь к здоровому телу сегодня</h2>
                <p>Подберите подходящую программу тренировок и питания для достижения ваших целей</p>
            </div>
        </section>
        
        <section id="methods">
            <h2>Методы похудения</h2>
            
            <div class="method-card">
                <div class="method-header" onclick="toggleMethod('morning')">
                    <h3>Утренняя гимнастика</h3>
                    <span class="method-icon">▼</span>
                </div>
                <div id="morning" class="method-content">
                    <div class="difficulty-tabs">
                        <div class="difficulty-tab active" onclick="changeDifficulty('morning', 'beginner')">Начинающий</div>
                        <div class="difficulty-tab" onclick="changeDifficulty('morning', 'intermediate')">Средний</div>
                        <div class="difficulty-tab" onclick="changeDifficulty('morning', 'advanced')">Продвинутый</div>
                    </div>
                    
                    <div id="morning-beginner" class="difficulty-content active">
                        <div class="exercise">
                            <h4>1. Разминка шеи <span class="duration">2 мин</span></h4>
                            <p>Наклоны головы вперед-назад, влево-вправо, круговые движения. Выполняйте плавно, без резких движений.</p>
                            <a href="https://www.youtube.com/watch?v=JZQA5SlNH4M" class="video-link" target="_blank">Смотреть упражнение</a>
                        </div>
                        <div class="exercise">
                            <h4>2. Вращения плечами <span class="duration">2 мин</span></h4>
                            <p>Вращайте плечами вперед и назад, сначала поочередно, затем вместе. Следите за осанкой.</p>
                            <a href="https://www.youtube.com/watch?v=6AeYf0e5X8w" class="video-link" target="_blank">Смотреть упражнение</a>
                        </div>
                        <div class="exercise">
                            <h4>3. Наклоны корпуса <span class="duration">3 мин</span></h4>
                            <p>Наклоны в стороны и вперед, руки вдоль тела или над головой. Держите спину прямой.</p>
                            <a href="https://www.youtube.com/watch?v=dmY4b5X5mYU" class="video-link" target="_blank">Смотреть упражнение</a>
                        </div>
                        <div class="exercise">
                            <h4>4. Приседания <span class="duration">3 мин</span></h4>
                            <p>3 подхода по 10 раз. Следите, чтобы колени не выходили за носки, спина прямая.</p>
                            <a href="https://www.youtube.com/watch?v=aclHkVaku9U" class="video-link" target="_blank">Смотреть упражнение</a>
                        </div>
                        <div class="exercise">
                            <h4>5. Отжимания от стены <span class="duration">3 мин</span></h4>
                            <p>3 подхода по 8 раз. Встаньте на расстоянии шага от стены, выполняйте отжимания, контролируя движение.</p>
                            <a href="https://www.youtube.com/watch?v=8wP6Yk--7gE" class="video-link" target="_blank">Смотреть упражнение</a>
                        </div>
                        <div class="exercise">
                            <h4>6. Планка на коленях <span class="duration">30 сек</span></h4>
                            <p>Удерживайте положение, опираясь на предплечья и колени. Тело прямое от головы до колен.</p>
                            <a href="https://www.youtube.com/watch?v=B296mZDhrP4" class="video-link" target="_blank">Смотреть упражнение</a>
                        </div>
                        <div class="exercise">
                            <h4>7. Растяжка <span class="duration">5 мин</span></h4>
                            <p>Растяните все основные группы мышц, уделяя внимание спине, ногам и рукам.</p>
                            <a href="https://www.youtube.com/watch?v=g_tea8ZNk5A" class="video-link" target="_blank">Смотреть комплекс</a>
                        </div>
                    </div>
                    
                    <div id="morning-intermediate" class="difficulty-content">
                        <div class="exercise">
                            <h4>1. Динамическая разминка <span class="duration">5 мин</span></h4>
                            <p>Комплекс включает махи руками и ногами, выпады на месте, круговые движения тазом.</p>
                            <a href="https://www.youtube.com/watch?v=oAPCPjnU1wA" class="video-link" target="_blank">Смотреть комплекс</a>
                        </div>
                        <div class="exercise">
                            <h4>2. Приседания с выпрыгиванием <span class="duration">3 мин</span></h4>
                            <p>3 подхода по 12 раз. Из приседа выпрыгивайте вверх, мягко приземляйтесь.</p>
                            <a href="https://www.youtube.com/watch?v=CVaEhXotL7M" class="video-link" target="_blank">Смотреть упражнение</a>
                        </div>
                        <div class="exercise">
                            <h4>3. Отжимания от пола <span class="duration">4 мин</span></h4>
                            <p>3 подхода по 10 раз. Тело прямое, локти близко к корпусу.</p>
                            <a href="https://www.youtube.com/watch?v=IODxDxX7oi4" class="video-link" target="_blank">Смотреть упражнение</a>
                        </div>
                        <div class="exercise">
                            <h4>4. Планка <span class="duration">1 мин</span></h4>
                            <p>Удерживайте положение на предплечьях и носках, тело прямое.</p>
                            <a href="https://www.youtube.com/watch?v=pSHjTRCQxIw" class="video-link" target="_blank">Смотреть упражнение</a>
                        </div>
                        <div class="exercise">
                            <h4>5. Бёрпи <span class="duration">3 мин</span></h4>
                            <p>3 подхода по 8 раз. Комбинация приседа, планки и прыжка.</p>
                            <a href="https://www.youtube.com/watch?v=auBLPXO8Fww" class="video-link" target="_blank">Смотреть упражнение</a>
                        </div>
                        <div class="exercise">
                            <h4>6. Скручивания <span class="duration">3 мин</span></h4>
                            <p>3 подхода по 15 раз. Поднимайте только лопатки, поясница прижата к полу.</p>
                            <a href="https://www.youtube.com/watch?v=1fbU_MkV7NE" class="video-link" target="_blank">Смотреть упражнение</a>
                        </div>
                        <div class="exercise">
                            <h4>7. Растяжка <span class="duration">5 мин</span></h4>
                            <p>Глубокое растяжение всех групп мышц с акцентом на ноги и спину.</p>
                            <a href="https://www.youtube.com/watch?v=4pKly2JojMw" class="video-link" target="_blank">Смотреть комплекс</a>
                        </div>
                    </div>
                    
                    <div id="morning-advanced" class="difficulty-content">
                        <div class="exercise">
                            <h4>1. Интенсивная разминка <span class="duration">7 мин</span></h4>
                            <p>Бег на месте, прыжки, махи, выпады в движении - комплекс для разогрева всех мышц.</p>
                            <a href="https://www.youtube.com/watch?v=jDwoBqPH0jk" class="video-link" target="_blank">Смотреть комплекс</a>
                        </div>
                        <div class="exercise">
                            <h4>2. Приседания с прыжком и поворотом <span class="duration">4 мин</span></h4>
                            <p>3 подхода по 15 раз. В прыжке поворачивайте корпус на 90 градусов.</p>
                            <a href="https://www.youtube.com/watch?v=GZbfZ1f_Xl0" class="video-link" target="_blank">Смотреть упражнение</a>
                        </div>
                        <div class="exercise">
                            <h4>3. Отжимания с хлопком <span class="duration">4 мин</span></h4>
                            <p>3 подхода по 10 раз. В верхней точке оторвите руки от пола и сделайте хлопок.</p>
                            <a href="https://www.youtube.com/watch?v=Eh00_rniF8E" class="video-link" target="_blank">Смотреть упражнение</a>
                        </div>
                        <div class="exercise">
                            <h4>4. Планка с подъемом ног <span class="duration">2 мин</span></h4>
                            <p>Поочередно поднимайте ноги, удерживая положение планки.</p>
                            <a href="https://www.youtube.com/watch?v=44ScXWFaVBs" class="video-link" target="_blank">Смотреть упражнение</a>
                        </div>
                        <div class="exercise">
                            <h4>5. Бёрпи с прыжком через препятствие <span class="duration">4 мин</span></h4>
                            <p>3 подхода по 10 раз. После прыжка вверх перепрыгните через воображаемое препятствие.</p>
                            <a href="https://www.youtube.com/watch?v=qLBImHhCXSw" class="video-link" target="_blank">Смотреть упражнение</a>
                        </div>
                        <div class="exercise">
                            <h4>6. Велосипед для пресса <span class="duration">4 мин</span></h4>
                            <p>3 подхода по 20 раз на каждую сторону. Локтем касайтесь противоположного колена.</p>
                            <a href="https://www.youtube.com/watch?v=9FGilxCbdz8" class="video-link" target="_blank">Смотреть упражнение</a>
                        </div>
                        <div class="exercise">
                            <h4>7. Глубокая растяжка <span class="duration">5 мин</span></h4>
                            <p>Растяжка с элементами йоги для повышения гибкости.</p>
                            <a href="https://www.youtube.com/watch?v=L_xrDAtykMI" class="video-link" target="_blank">Смотреть комплекс</a>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="method-card">
                <div class="method-header" onclick="toggleMethod('yoga')">
                    <h3>Йога для похудения</h3>
                    <span class="method-icon">▼</span>
                </div>
                <div id="yoga" class="method-content">
                    <div class="difficulty-tabs">
                        <div class="difficulty-tab active" onclick="changeDifficulty('yoga', 'beginner')">Начинающий</div>
                        <div class="difficulty-tab" onclick="changeDifficulty('yoga', 'intermediate')">Средний</div>
                        <div class="difficulty-tab" onclick="changeDifficulty('yoga', 'advanced')">Продвинутый</div>
                    </div>
                    
                    <div id="yoga-beginner" class="difficulty-content active">
                        <div class="exercise">
                            <h4>1. Поза горы (Тадасана) <span class="duration">2 мин</span></h4>
                            <p>Стоя прямо, распределите вес равномерно на обе стопы. Дышите глубоко.</p>
                            <a href="https://www.youtube.com/watch?v=U3nZqDz3QnQ" class="video-link" target="_blank">Смотреть позу</a>
                        </div>
                        <div class="exercise">
                            <h4>2. Поза дерева (Врикшасана) <span class="duration">2 мин на каждую сторону</span></h4>
                            <p>Стоя на одной ноге, вторую стопу поместите на внутреннюю часть бедра.</p>
                            <a href="https://www.youtube.com/watch?v=2d2cs2QlJvY" class="video-link" target="_blank">Смотреть позу</a>
                        </div>
                        <div class="exercise">
                            <h4>3. Поза воина I (Вирабхадрасана I) <span class="duration">2 мин на каждую сторону</span></h4>
                            <p>Широкий выпад вперед, руки подняты вверх, задняя нога прямая.</p>
                            <a href="https://www.youtube.com/watch?v=OZBW9I3mCz8" class="video-link" target="_blank">Смотреть позу</a>
                        </div>
                        <div class="exercise">
                            <h4>4. Поза собаки мордой вниз (Адхо Мукха Шванасана) <span class="duration">3 мин</span></h4>
                            <p>Тело образует треугольник, пятки стремятся к полу.</p>
                            <a href="https://www.youtube.com/watch?v=0iS0HXJh-1s" class="video-link" target="_blank">Смотреть позу</a>
                        </div>
                        <div class="exercise">
                            <h4>5. Поза ребенка (Баласана) <span class="duration">3 мин</span></h4>
                            <p>Колени широко, ягодицы на пятках, лоб на полу, руки вытянуты вперед.</p>
                            <a href="https://www.youtube.com/watch?v=2MJGg-dUKh0" class="video-link" target="_blank">Смотреть позу</a>
                        </div>
                        <div class="exercise">
                            <h4>6. Поза кобры (Бхуджангасана) <span class="duration">2 мин</span></h4>
                            <p>Лежа на животе, поднимите верхнюю часть тела, опираясь на ладони.</p>
                            <a href="https://www.youtube.com/watch?v=JDcdhTuycOI" class="video-link" target="_blank">Смотреть позу</a>
                        </div>
                        <div class="exercise">
                            <h4>7. Шавасана (поза расслабления) <span class="duration">5 мин</span></h4>
                            <p>Лежа на спине, полностью расслабьте все тело, сосредоточьтесь на дыхании.</p>
                            <a href="https://www.youtube.com/watch?v=5j7X4oK0P7s" class="video-link" target="_blank">Смотреть позу</a>
                        </div>
                    </div>
                    
                    <div id="yoga-intermediate" class="difficulty-content">
                        <div class="exercise">
                            <h4>1. Приветствие солнцу (Сурья Намаскар) <span class="duration">5 мин</span></h4>
                            <p>Комплекс из 12 последовательных поз, выполняемых в потоке.</p>
                            <a href="https://www.youtube.com/watch?v=5_ZsD1w6c3Y" class="video-link" target="_blank">Смотреть комплекс</a>
                        </div>
                        <div class="exercise">
                            <h4>2. Поза воина II (Вирабхадрасана II) <span class="duration">3 мин на каждую сторону</span></h4>
                            <p>Широкий выпад, руки разведены в стороны, взгляд поверх передней руки.</p>
                            <a href="https://www.youtube.com/watch?v=8Iqmd1BZP1Y" class="video-link" target="_blank">Смотреть позу</a>
                        </div>
                        <div class="exercise">
                            <h4>3. Поза треугольника (Триконасана) <span class="duration">3 мин на каждую сторону</span></h4>
                            <p>Ноги широко, наклон к одной ноге, рука касается голени или пола.</p>
                            <a href="https://www.youtube.com/watch?v=S6gB0QHbWFE" class="video-link" target="_blank">Смотреть позу</a>
                        </div>
                        <div class="exercise">
                            <h4>4. Поза лука (Дханурасана) <span class="duration">2 мин</span></h4>
                            <p>Лежа на животе, возьмитесь за лодыжки и поднимите корпус и ноги.</p>
                            <a href="https://www.youtube.com/watch?v=QFzz9T5WrE0" class="video-link" target="_blank">Смотреть позу</a>
                        </div>
                        <div class="exercise">
                            <h4>5. Поза лодки (Навасана) <span class="duration">3 подхода по 30 сек</span></h4>
                            <p>Баланс на ягодицах, ноги и корпус подняты, руки параллельно полу.</p>
                            <a href="https://www.youtube.com/watch?v=9a6Ji3g8b4o" class="video-link" target="_blank">Смотреть позу</a>
                        </div>
                        <div class="exercise">
                            <h4>6. Поза саранчи (Шалабхасана) <span class="duration">2 мин</span></h4>
                            <p>Лежа на животе, поднимите грудь и ноги, руки вдоль тела.</p>
                            <a href="https://www.youtube.com/watch?v=Y7IuwZFz9X4" class="video-link" target="_blank">Смотреть позу</a>
                        </div>
                        <div class="exercise">
                            <h4>7. Медитация <span class="duration">5 мин</span></h4>
                            <p>Сидя с прямой спиной, сосредоточьтесь на дыхании, отпустите мысли.</p>
                            <a href="https://www.youtube.com/watch?v=O-6f5wQXSu8" class="video-link" target="_blank">Смотреть технику</a>
                        </div>
                    </div>
                    
                    <div id="yoga-advanced" class="difficulty-content">
                        <div class="exercise">
                            <h4>1. Приветствие солнцу (ускоренный вариант) <span class="duration">5 мин</span></h4>
                            <p>Быстрое выполнение комплекса с акцентом на дыхание.</p>
                            <a href="https://www.youtube.com/watch?v=b1H3xO3x_Js" class="video-link" target="_blank">Смотреть комплекс</a>
                        </div>
                        <div class="exercise">
                            <h4>2. Поза воина III (Вирабхадрасана III) <span class="duration">2 мин на каждую сторону</span></h4>
                            <p>Баланс на одной ноге, корпус и вторая нога параллельны полу.</p>
                            <a href="https://www.youtube.com/watch?v=5S6T7FV3T-8" class="video-link" target="_blank">Смотреть позу</a>
                        </div>
                        <div class="exercise">
                            <h4>3. Поза ворона (Бакасана) <span class="duration">3 подхода по 30 сек</span></h4>
                            <p>Баланс на руках, колени на задней поверхности плеч.</p>
                            <a href="https://www.youtube.com/watch?v=TYk1eD5sX3I" class="video-link" target="_blank">Смотреть позу</a>
                        </div>
                        <div class="exercise">
                            <h4>4. Поза колеса (Чакрасана) <span class="duration">3 мин</span></h4>
                            <p>Мост с прямыми руками, максимальный прогиб в спине.</p>
                            <a href="https://www.youtube.com/watch?v=7Zk1uH7TQhA" class="video-link" target="_blank">Смотреть позу</a>
                        </div>
                        <div class="exercise">
                            <h4>5. Поза стула с поворотом (Паривритта Уткатасана) <span class="duration">2 мин на каждую сторону</span></h4>
                            <p>Присед с поворотом корпуса, локтем за противоположное колено.</p>
                            <a href="https://www.youtube.com/watch?v=0mFj8T5kQ4Q" class="video-link" target="_blank">Смотреть позу</a>
                        </div>
                        <div class="exercise">
                            <h4>6. Поза короля танцоров (Натараджасана) <span class="duration">2 мин на каждую сторону</span></h4>
                            <p>Баланс на одной ноге, вторая нога согнута и отведена назад.</p>
                            <a href="https://www.youtube.com/watch?v=5UQ60VQZg3k" class="video-link" target="_blank">Смотреть позу</a>
                        </div>
                        <div class="exercise">
                            <h4>7. Глубокая медитация <span class="duration">10 мин</span></h4>
                            <p>Продвинутые техники концентрации и осознанности.</p>
                            <a href="https://www.youtube.com/watch?v=O-6f5wQXSu8" class="video-link" target="_blank">Смотреть технику</a>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="method-card">
                <div class="method-header" onclick="toggleMethod('dance')">
                    <h3>Танцевальная гимнастика</h3>
                    <span class="method-icon">▼</span>
                </div>
                <div id="dance" class="method-content">
                    <div class="difficulty-tabs">
                        <div class="difficulty-tab active" onclick="changeDifficulty('dance', 'beginner')">Начинающий</div>
                        <div class="difficulty-tab" onclick="changeDifficulty('dance', 'intermediate')">Средний</div>
                        <div class="difficulty-tab" onclick="changeDifficulty('dance', 'advanced')">Продвинутый</div>
                    </div>
                    
                    <div id="dance-beginner" class="difficulty-content active">
                        <div class="exercise">
                            <h4>1. Разминка под музыку <span class="duration">5 мин</span></h4>
                            <p>Простые движения на разогрев: шаги, махи руками, повороты.</p>
                            <a href="https://www.youtube.com/watch?v=2j8XZxQf0Jw" class="video-link" target="_blank">Смотреть разминку</a>
                        </div>
                        <div class="exercise">
                            <h4>2. Базовые шаги зумбы <span class="duration">10 мин</span></h4>
                            <p>Освоение основных шагов: меренге, сальса, реггетон.</p>
                            <a href="https://www.youtube.com/watch?v=vj0rw1LwL1E" class="video-link" target="_blank">Смотреть шаги</a>
                        </div>
                        <div class="exercise">
                            <h4>3. Простая комбинация <span class="duration">8 мин</span></h4>
                            <p>Соединение выученных шагов в простую танцевальную связку.</p>
                            <a href="https://www.youtube.com/watch?v=3A5Qq4z1R00" class="video-link" target="_blank">Смотреть комбинацию</a>
                        </div>
                        <div class="exercise">
                            <h4>4. Заминка и растяжка <span class="duration">7 мин</span></h4>
                            <p>Медленные движения на растяжку основных групп мышц.</p>
                            <a href="https://www.youtube.com/watch?v=4pKly2JojMw" class="video-link" target="_blank">Смотреть заминку</a>
                        </div>
                    </div>
                    
                    <div id="dance-intermediate" class="difficulty-content">
                        <div class="exercise">
                            <h4>1. Интенсивная разминка <span class="duration">7 мин</span></h4>
                            <p>Динамичные движения с элементами латины и хип-хопа.</p>
                            <a href="https://www.youtube.com/watch?v=5j7X4oK0P7s" class="video-link" target="_blank">Смотреть разминку</a>
                        </div>
                        <div class="exercise">
                            <h4>2. Комбинация зумбы среднего уровня <span class="duration">12 мин</span></h4>
                            <p>Более сложные связки с добавлением поворотов и движений руками.</p>
                            <a href="https://www.youtube.com/watch?v=Y1Fxn8C7h0s" class="video-link" target="_blank">Смотреть комбинацию</a>
                        </div>
                        <div class="exercise">
                            <h4>3. Танцевальный интервал <span class="duration">8 мин</span></h4>
                            <p>Чередование быстрых и медленных движений для интервального эффекта.</p>
                            <a href="https://www.youtube.com/watch?v=3A5Qq4z1R00" class="video-link" target="_blank">Смотреть интервалы</a>
                        </div>
                        <div class="exercise">
                            <h4>4. Растяжка и расслабление <span class="duration">8 мин</span></h4>
                            <p>Глубокая растяжка с элементами современного танца.</p>
                            <a href="https://www.youtube.com/watch?v=L_xrDAtykMI" class="video-link" target="_blank">Смотреть растяжку</a>
                        </div>
                    </div>
                    
                    <div id="dance-advanced" class="difficulty-content">
                        <div class="exercise">
                            <h4>1. Кардио-разминка <span class="duration">10 мин</span></h4>
                            <p>Высокоинтенсивные движения для быстрого разогрева.</p>
                            <a href="https://www.youtube.com/watch?v=jDwoBqPH0jk" class="video-link" target="_blank">Смотреть разминку</a>
                        </div>
                        <div class="exercise">
                            <h4>2. Продвинутая зумба-комбинация <span class="duration">15 мин</span></h4>
                            <p>Сложные связки с быстрой сменой направлений и уровней.</p>
                            <a href="https://www.youtube.com/watch?v=Y1Fxn8C7h0s" class="video-link" target="_blank">Смотреть комбинацию</a>
                        </div>
                        <div class="exercise">
                            <h4>3. Фристайл и импровизация <span class="duration">10 мин</span></h4>
                            <p>Свободный танец с использованием изученных элементов.</p>
                            <a href="https://www.youtube.com/watch?v=3A5Qq4z1R00" class="video-link" target="_blank">Смотреть примеры</a>
                        </div>
                        <div class="exercise">
                            <h4>4. Профессиональная растяжка <span class="duration">10 мин</span></h4>
                            <p>Глубокая растяжка с элементами балета и contemporary.</p>
                            <a href="https://www.youtube.com/watch?v=L_xrDAtykMI" class="video-link" target="_blank">Смотреть растяжку</a>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="method-card">
                <div class="method-header" onclick="toggleMethod('hiit')">
                    <h3>HIIT тренировка</h3>
                    <span class="method-icon">▼</span>
                </div>
                <div id="hiit" class="method-content">
                    <div class="difficulty-tabs">
                        <div class="difficulty-tab active" onclick="changeDifficulty('hiit', 'beginner')">Начинающий</div>
                        <div class="difficulty-tab" onclick="changeDifficulty('hiit', 'intermediate')">Средний</div>
                        <div class="difficulty-tab" onclick="changeDifficulty('hiit', 'advanced')">Продвинутый</div>
                    </div>
                    
                    <div id="hiit-beginner" class="difficulty-content active">
                        <div class="exercise">
                            <h4>1. Разминка <span class="duration">5 мин</span></h4>
                            <p>Ходьба на месте, махи руками, наклоны, вращения суставов.</p>
                            <a href="https://www.youtube.com/watch?v=oAPCPjnU1wA" class="video-link" target="_blank">Смотреть разминку</a>
                        </div>
                        <div class="exercise">
                            <h4>2. Марш на месте с высоким подниманием колен <span class="duration">30 сек работа / 30 сек отдых</span></h4>
                            <p>3 цикла. Поднимайте колени как можно выше.</p>
                            <a href="https://www.youtube.com/watch?v=1TvsaPJ8Lzw" class="video-link" target="_blank">Смотреть упражнение</a>
                        </div>
                        <div class="exercise">
                            <h4>3. Приседания <span class="duration">30 сек / 30 сек</span></h4>
                            <p>3 цикла. Колени не выходят за носки, спина прямая.</p>
                            <a href="https://www.youtube.com/watch?v=aclHkVaku9U" class="video-link" target="_blank">Смотреть упражнение</a>
                        </div>
                        <div class="exercise">
                            <h4>4. Отжимания от стола или стула <span class="duration">30 сек / 30 сек</span></h4>
                            <p>3 цикла. Тело прямое, локти близко к корпусу.</p>
                            <a href="https://www.youtube.com/watch?v=8wP6Yk--7gE" class="video-link" target="_blank">Смотреть упражнение</a>
                        </div>
                        <div class="exercise">
                            <h4>5. Планка на коленях <span class="duration">30 сек / 30 сек</span></h4>
                            <p>3 цикла. Удерживайте прямое положение тела.</p>
                            <a href="https://www.youtube.com/watch?v=B296mZDhrP4" class="video-link" target="_blank">Смотреть упражнение</a>
                        </div>
                        <div class="exercise">
                            <h4>6. Заминка и растяжка <span class="duration">5 мин</span></h4>
                            <p>Медленные движения для восстановления дыхания и растяжки мышц.</p>
                            <a href="https://www.youtube.com/watch?v=g_tea8ZNk5A" class="video-link" target="_blank">Смотреть заминку</a>
                        </div>
                    </div>
                    
                    <div id="hiit-intermediate" class="difficulty-content">
                        <div class="exercise">
                            <h4>1. Разминка <span class="duration">5 мин</span></h4>
                            <p>Бег на месте, прыжки, махи, выпады - комплекс для разогрева.</p>
                            <a href="https://www.youtube.com/watch?v=jDwoBqPH0jk" class="video-link" target="_blank">Смотреть разминку</a>
                        </div>
                        <div class="exercise">
                            <h4>2. Прыжки с приседом (Jump Squats) <span class="duration">40 сек работа / 20 сек отдых</span></h4>
                            <p>4 цикла. Из приседа выпрыгивайте вверх, мягко приземляйтесь.</p>
                            <a href="https://www.youtube.com/watch?v=CVaEhXotL7M" class="video-link" target="_blank">Смотреть упражнение</a>
                        </div>
                        <div class="exercise">
                            <h4>3. Бёрпи <span class="duration">40 сек / 20 сек</span></h4>
                            <p>4 цикла. Комбинация приседа, планки и прыжка.</p>
                            <a href="https://www.youtube.com/watch?v=auBLPXO8Fww" class="video-link" target="_blank">Смотреть упражнение</a>
                        </div>
                        <div class="exercise">
                            <h4>4. Альпинист (Mountain Climbers) <span class="duration">40 сек / 20 сек</span></h4>
                            <p>4 цикла. В планке поочередно подтягивайте колени к груди.</p>
                            <a href="https://www.youtube.com/watch?v=nmwgirgXLYM" class="video-link" target="_blank">Смотреть упражнение</a>
                        </div>
                        <div class="exercise">
                            <h4>5. Планка с подъемом ног <span class="duration">40 сек / 20 сек</span></h4>
                            <p>4 цикла. Поочередно поднимайте ноги, удерживая положение.</p>
                            <a href="https://www.youtube.com/watch?v=44ScXWFaVBs" class="video-link" target="_blank">Смотреть упражнение</a>
                        </div>
                        <div class="exercise">
                            <h4>6. Заминка и растяжка <span class="duration">7 мин</span></h4>
                            <p>Глубокая растяжка всех групп мышц.</p>
                            <a href="https://www.youtube.com/watch?v=4pKly2JojMw" class="video-link" target="_blank">Смотреть заминку</a>
                        </div>
                    </div>
                    
                    <div id="hiit-advanced" class="difficulty-content">
                        <div class="exercise">
                            <h4>1. Интенсивная разминка <span class="duration">7 мин</span></h4>
                            <p>Высокоинтенсивные движения для максимального разогрева.</p>
                            <a href="https://www.youtube.com/watch?v=jDwoBqPH0jk" class="video-link" target="_blank">Смотреть разминку</a>
                        </div>
                        <div class="exercise">
                            <h4>2. Бёрпи с прыжком через препятствие <span class="duration">45 сек работа / 15 сек отдых</span></h4>
                            <p>5 циклов. После прыжка вверх перепрыгните через воображаемое препятствие.</p>
                            <a href="https://www.youtube.com/watch?v=qLBImHhCXSw" class="video-link" target="_blank">Смотреть упражнение</a>
                        </div>
                        <div class="exercise">
                            <h4>3. Прыжки в планке (Plank Jacks) <span class="duration">45 сек / 15 сек</span></h4>
                            <p>5 циклов. В планке прыжком разводите и сводите ноги.</p>
                            <a href="https://www.youtube.com/watch?v=Eh00_rniF8E" class="video-link" target="_blank">Смотреть упражнение</a>
                        </div>
                        <div class="exercise">
                            <h4>4. Приседания с выпрыгиванием и поворотом <span class="duration">45 сек / 15 сек</span></h4>
                            <p>5 циклов. В прыжке поворачивайте корпус на 90 градусов.</p>
                            <a href="https://www.youtube.com/watch?v=GZbfZ1f_Xl0" class="video-link" target="_blank">Смотреть упражнение</a>
                        </div>
                        <div class="exercise">
                            <h4>5. Отжимания с хлопком <span class="duration">45 сек / 15 сек</span></h4>
                            <p>5 циклов. В верхней точке оторвите руки от пола и сделайте хлопок.</p>
                            <a href="https://www.youtube.com/watch?v=Eh00_rniF8E" class="video-link" target="_blank">Смотреть упражнение</a>
                        </div>
                        <div class="exercise">
                            <h4>6. Глубокая растяжка <span class="duration">10 мин</span></h4>
                            <p>Растяжка с элементами йоги для повышения гибкости.</p>
                            <a href="https://www.youtube.com/watch?v=L_xrDAtykMI" class="video-link" target="_blank">Смотреть заминку</a>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="method-card">
                <div class="method-header" onclick="toggleMethod('western')">
                    <h3>Западные методы</h3>
                    <span class="method-icon">▼</span>
                </div>
                <div id="western" class="method-content">
                    <div class="difficulty-tabs">
                        <div class="difficulty-tab active" onclick="changeDifficulty('western', 'beginner')">Начинающий</div>
                        <div class="difficulty-tab" onclick="changeDifficulty('western', 'intermediate')">Средний</div>
                        <div class="difficulty-tab" onclick="changeDifficulty('western', 'advanced')">Продвинутый</div>
                    </div>
                    
                    <div id="western-beginner" class="difficulty-content active">
                        <div class="exercise">
                            <h4>1. Кардио на эллипсоиде <span class="duration">20 мин</span></h4>
                            <p>Умеренный темп с сопротивлением, которое позволяет поддерживать разговор.</p>
                            <a href="https://www.youtube.com/watch?v=Q5c3lDhJebk" class="video-link" target="_blank">Смотреть технику</a>
                        </div>
                        <div class="exercise">
                            <h4>2. Тренировка с резиновыми лентами <span class="duration">15 мин</span></h4>
                            <p>Базовые упражнения на все группы мышц с минимальным сопротивлением.</p>
                            <a href="https://www.youtube.com/watch?v=2T6PrWi0kDk" class="video-link" target="_blank">Смотреть комплекс</a>
                        </div>
                        <div class="exercise">
                            <h4>3. Растяжка на фитболе <span class="duration">5 мин</span></h4>
                            <p>Мягкая растяжка с использованием фитбола для расслабления мышц.</p>
                            <a href="https://www.youtube.com/watch?v=5j7X4oK0P7s" class="video-link" target="_blank">Смотреть упражнения</a>
                        </div>
                    </div>
                    
                    <div id="western-intermediate" class="difficulty-content">
                        <div class="exercise">
                            <h4>1. Интервалы на беговой дорожке <span class="duration">25 мин</span></h4>
                            <p>Чередование 1 мин быстрого бега и 2 мин ходьбы.</p>
                            <a href="https://www.youtube.com/watch?v=5j7X4oK0P7s" class="video-link" target="_blank">Смотреть программу</a>
                        </div>
                        <div class="exercise">
                            <h4>2. Круговая тренировка с гантелями <span class="duration">20 мин</span></h4>
                            <p>3 круга по 8 упражнений (12 повторений каждое) с небольшими весами.</p>
                            <a href="https://www.youtube.com/watch?v=2T6PrWi0kDk" class="video-link" target="_blank">Смотреть комплекс</a>
                        </div>
                        <div class="exercise">
                            <h4>3. Пилатес реформер <span class="duration">15 мин</span></h4>
                            <p>Упражнения на укрепление корпуса и улучшение осанки.</p>
                            <a href="https://www.youtube.com/watch?v=5j7X4oK0P7s" class="video-link" target="_blank">Смотреть упражнения</a>
                        </div>
                    </div>
                    
                    <div id="western-advanced" class="difficulty-content">
                        <div class="exercise">
                            <h4>1. Спринтерские интервалы <span class="duration">30 мин</span></h4>
                            <p>30 сек максимального спринта, 1 мин отдыха - 15 циклов.</p>
                            <a href="https://www.youtube.com/watch?v=5j7X4oK0P7s" class="video-link" target="_blank">Смотреть технику</a>
                        </div>
                        <div class="exercise">
                            <h4>2. Кроссфит WOD <span class="duration">20 мин</span></h4>
                            <p>Комплекс из приседаний со штангой, подтягиваний и бёрпи на время.</p>
                            <a href="https://www.youtube.com/watch?v=5j7X4oK0P7s" class="video-link" target="_blank">Смотреть комплекс</a>
                        </div>
                        <div class="exercise">
                            <h4>3. TRX полная тренировка <span class="duration">20 мин</span></h4>
                            <p>Упражнения на все группы мышц с использованием подвесных петель.</p>
                            <a href="https://www.youtube.com/watch?v=5j7X4oK0P7s" class="video-link" target="_blank">Смотреть упражнения</a>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        
        <section id="difficulty">
            <h2>Тренировки по сложности</h2>
            
            <div class="method-card">
                <div class="method-header" onclick="toggleMethod('beginner-level')">
                    <h3>Для начинающих</h3>
                    <span class="method-icon">▼</span>
                </div>
                <div id="beginner-level" class="method-content">
                    <p>Эти тренировки подходят для тех, кто только начинает свой путь к здоровому образу жизни или возвращается к физической активности после перерыва.</p>
                    
                    <h4>Пример недельного плана:</h4>
                    <ul>
                        <li><strong>Понедельник:</strong> Утренняя гимнастика (начальный уровень) - 20 мин</li>
                        <li><strong>Вторник:</strong> Прогулка быстрым шагом - 30 мин</li>
                        <li><strong>Среда:</strong> Йога для начинающих - 25 мин</li>
                        <li><strong>Четверг:</strong> Отдых или легкая растяжка</li>
                        <li><strong>Пятница:</strong> Танцевальная гимнастика (начальный уровень) - 25 мин</li>
                        <li><strong>Суббота:</strong> Прогулка на природе - 40 мин</li>
                        <li><strong>Воскресенье:</strong> Отдых</li>
                    </ul>
                    
                    <div class="exercise">
                        <h4>Советы для начинающих:</h4>
                        <p>1. Начинайте с малого - даже 10 минут активности лучше, чем ничего.</p>
                        <p>2. Следите за техникой выполнения упражнений, а не за скоростью.</p>
                        <p>3. Не пропускайте разминку и заминку - они предотвращают травмы.</p>
                        <p>4. Пейте воду до, во время и после тренировки.</p>
                        <p>5. Прислушивайтесь к своему телу - боль это сигнал остановиться.</p>
                    </div>
                </div>
            </div>
            
            <div class="method-card">
                <div class="method-header" onclick="toggleMethod('intermediate-level')">
                    <h3>Средний уровень</h3>
                    <span class="method-icon">▼</span>
                </div>
                <div id="intermediate-level" class="method-content">
                    <p>Для тех, кто уже имеет базовый уровень подготовки и готов к более интенсивным нагрузкам.</p>
                    
                    <h4>Пример недельного плана:</h4>
                    <ul>
                        <li><strong>Понедельник:</strong> HIIT тренировка (средний уровень) - 25 мин</li>
                        <li><strong>Вторник:</strong> Йога среднего уровня - 30 мин</li>
                        <li><strong>Среда:</strong> Силовая тренировка с собственным весом - 30 мин</li>
                        <li><strong>Четверг:</strong> Активное восстановление (плавание, велосипед) - 40 мин</li>
                        <li><strong>Пятница:</strong> Танцевальная гимнастика (средний уровень) - 30 мин</li>
                        <li><strong>Суббота:</strong> Длительная кардионагрузка (бег, велосипед) - 45 мин</li>
                        <li><strong>Воскресенье:</strong> Отдых или легкая растяжка</li>
                    </ul>
                    
                    <div class="exercise">
                        <h4>Советы для среднего уровня:</h4>
                        <p>1. Добавляйте разнообразие в тренировки для всестороннего развития.</p>
                        <p>2. Увеличивайте интенсивность постепенно - не более 10% в неделю.</p>
                        <p>3. Включайте силовые упражнения для ускорения метаболизма.</p>
                        <p>4. Следите за восстановлением - мышцы растут во время отдыха.</p>
                        <p>5. Экспериментируйте с разными видами активности.</p>
                    </div>
                </div>
            </div>
            
            <div class="method-card">
                <div class="method-header" onclick="toggleMethod('advanced-level')">
                    <h3>Продвинутый уровень</h3>
                    <span class="method-icon">▼</span>
                </div>
                <div id="advanced-level" class="method-content">
                    <p>Для опытных спортсменов, которые хотят выйти на новый уровень физической подготовки.</p>
                    
                    <h4>Пример недельного плана:</h4>
                    <ul>
                        <li><strong>Понедельник:</strong> HIIT продвинутый уровень - 30 мин + силовая</li>
                        <li><strong>Вторник:</strong> Продвинутая йога - 40 мин</li>
                        <li><strong>Среда:</strong> Кроссфит WOD - 35 мин</li>
                        <li><strong>Четверг:</strong> Интервальный бег - 45 мин</li>
                        <li><strong>Пятница:</strong> TRX или функциональный тренинг - 40 мин</li>
                        <li><strong>Суббота:</strong> Длительная интенсивная тренировка - 60 мин</li>
                        <li><strong>Воскресенье:</strong> Активное восстановление или отдых</li>
                    </ul>
                    
                    <div class="exercise">
                        <h4>Советы для продвинутого уровня:</h4>
                        <p>1. Разработайте четкий план с конкретными целями.</p>
                        <p>2. Используйте принцип периодизации для предотвращения плато.</p>
                        <p>3. Включайте элементы суперсетов и дроп-сетов.</p>
                        <p>4. Следите за питанием и восстановлением - они критически важны.</p>
                        <p>5. Регулярно меняйте программу, чтобы шокировать мышцы.</p>
                    </div>
                </div>
            </div>
        </section>
        
        <section id="nutrition" class="progress-section">
            <h2>Правильное питание</h2>
            <p>Здоровое питание - это 70% успеха в похудении. Вот основные принципы:</p>
            
            <div class="nutrition-tips">
                <div class="tip-card">
                    <h4>Баланс нутриентов</h4>
                    <p>Оптимальное соотношение: 30% белки, 30% жиры, 40% углеводы. Увеличивайте белок для сохранения мышц.</p>
                </div>
                <div class="tip-card">
                    <h4>Режим питания</h4>
                    <p>5-6 небольших приемов пищи в день с интервалом 2,5-3 часа. Не пропускайте завтрак!</p>
                </div>
                <div class="tip-card">
                    <h4>Вода</h4>
                    <p>30-40 мл воды на 1 кг веса в день. Стакан воды за 30 мин до еды снижает аппетит.</p>
                </div>
                <div class="tip-card">
                    <h4>Полезные продукты</h4>
                    <p>Овощи, нежирное мясо, рыба, яйца, крупы, бобовые, орехи, кисломолочные продукты.</p>
                </div>
                <div class="tip-card">
                    <h4>Вредные продукты</h4>
                    <p>Сахар, белая мука, фастфуд, сладкие напитки, трансжиры, алкоголь.</p>
                </div>
                <div class="tip-card">
                    <h4>Дефицит калорий</h4>
                    <p>Для похудения потребляйте на 10-20% меньше калорий, чем тратите. Не менее 1200 ккал/день!</p>
                </div>
            </div>
            
            <h3>Пример дневного рациона</h3>
            <div class="nutrition-tips">
                <div class="tip-card">
                    <h4>Завтрак</h4>
                    <p>Овсянка на воде с ягодами и орехами + яйцо всмятку + зеленый чай</p>
                </div>
                <div class="tip-card">
                    <h4>Перекус</h4>
                    <p>Творог с огурцом и зеленью + горсть миндаля</p>
                </div>
                <div class="tip-card">
                    <h4>Обед</h4>
                    <p>Гречка + запеченная куриная грудка + салат из овощей с оливковым маслом</p>
                </div>
                <div class="tip-card">
                    <h4>Полдник</h4>
                    <p>Яблоко + натуральный йогурт без добавок</p>
                </div>
                <div class="tip-card">
                    <h4>Ужин</h4>
                    <p>Запеченная рыба + тушеные овощи + авокадо</p>
                </div>
                <div class="tip-card">
                    <h4>Перед сном</h4>
                    <p>Стакан кефира или порция творога</p>
                </div>
            </div>
        </section>
        
        <section id="progress" class="progress-section">
            <h2>Отслеживание прогресса</h2>
            <p>Регулярное отслеживание параметров поможет вам оставаться мотивированными и корректировать программу.</p>
            
            <div class="progress-form">
                <div class="form-group">
                    <label for="weight">Вес (кг)</label>
                    <input type="number" id="weight" step="0.1">
                </div>
                <div class="form-group">
                    <label for="waist">Объем талии (см)</label>
                    <input type="number" id="waist">
                </div>
                <div class="form-group">
                    <label for="hips">Объем бедер (см)</label>
                    <input type="number" id="hips">
                </div>
                <div class="form-group">
                    <label for="chest">Объем груди (см)</label>
                    <input type="number" id="chest">
                </div>
                <div class="form-group">
                    <label for="date">Дата измерения</label>
                    <input type="date" id="date">
                </div>
                <div class="form-group">
                    <label for="workout">Тренировка</label>
                    <select id="workout">
                        <option value="">Выберите тип тренировки</option>
                        <option value="morning">Утренняя гимнастика</option>
                        <option value="yoga">Йога</option>
                        <option value="dance">Танцевальная гимнастика</option>
                        <option value="hiit">HIIT</option>
                        <option value="western">Западные методы</option>
                    </select>
                </div>
            </div>
            <button onclick="saveProgress()">Сохранить данные</button>
            
            <h3>Советы по отслеживанию:</h3>
            <ul>
                <li>Взвешивайтесь утром натощак после туалета 1 раз в неделю</li>
                <li>Делайте замеры объемов в одних и тех же местах</li>
                <li>Фотографируйтесь в одинаковой одежде/позе каждые 2 недели</li>
                <li>Записывайте свои тренировки и ощущения</li>
                <li>Отмечайте изменения в качестве сна, энергии, настроении</li>
            </ul>
        </section>
    </div>
    
    <footer>
        <p>&copy; 2023 Путь к стройности. Все права защищены.</p>
        <p>Перед началом любой программы проконсультируйтесь с врачом.</p>
    </footer>
    
    <script>
        // Переключение методов
        function toggleMethod(methodId) {
            const method = document.getElementById(methodId);
            method.classList.toggle('active');
            const header = method.previousElementSibling;
            header.classList.toggle('active');
        }
        
        // Изменение сложности
        function changeDifficulty(method, level) {
            // Скрыть все вкладки сложности для этого метода
            const tabs = document.querySelectorAll(#${method} .difficulty-content);
            tabs.forEach(tab => tab.classList.remove('active'));
            
            // Показать выбранную вкладку
            document.getElementById(${method}-${level}).classList.add('active');
            
            // Обновить активные табы
            const tabButtons = document.querySelectorAll(#${method} .difficulty-tab);
            tabButtons.forEach(btn => btn.classList.remove('active'));
            event.target.classList.add('active');
        }
        
        // Сохранение прогресса
        function saveProgress() {
            const weight = document.getElementById('weight').value;
            const waist = document.getElementById('waist').value;
            const hips = document.getElementById('hips').value;
            const chest = document.getElementById('chest').value;
            const date = document.getElementById('date').value;
            const workout = document.getElementById('workout').value;
            
            if (!weight || !date) {
                alert('Пожалуйста, заполните как минимум вес и дату');
                return;
            }
            
            // Здесь можно добавить код для сохранения данных (localStorage или отправка на сервер)
            alert(Данные за ${date} сохранены!\nВес: ${weight} кг\nТалия: ${waist || '-'} см\nБедра: ${hips || '-'} см\nГрудь: ${chest || '-'} см\nТренировка: ${workout || 'не указана'});
            
            // Очистка формы
            document.getElementById('weight').value = '';
            document.getElementById('waist').value = '';
            document.getElementById('hips').value = '';
            document.getElementById('chest').value = '';
            document.getElementById('date').value = '';
            document.getElementById('workout').value = '';
        }
        
        // Автоматическое открытие соответствующего раздела при переходе по якорю
        window.addEventListener('load', function() {
            if (window.location.hash) {
                const target = document.querySelector(window.location.hash);
                if (target && target.classList.contains('method-header')) {
                    toggleMethod(target.nextElementSibling.id);
                }
            }
        });
    </script>
</body>
</html>
