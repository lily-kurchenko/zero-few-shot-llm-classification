# zero-few-shot-llm-classification

В данном исследовании мы оценивали производительность различных мо-
делей, включая Mistral-7B и LLaMA-3-8B, в сценариях zero-shot, 5-shot и 10-shot
на наборах данных RuSentiment, IMDB и Inappropriate Sensitive Topics. Наша
цель заключалась в том, чтобы понять, как качество классификации зависит
от количества примеров на класс, исследовать устойчивость моделей к замене
примеров в промптах и определить влияние размера и архитектуры моделей на
качество классификации.
Результаты показали значительное улучшение precision, recall и F1-score
с увеличением числа примеров. Модели хорошо справлялись с классификацией
знакомых классов, таких как "Positive"и "Negative но испытывали трудности
с менее знакомыми классами, такими как "Skip"и "Speech что указывает на
необходимость большего объема данных и более глубокого обучения для этих
категорий.
Мы использовали квантизацию как способ оптимизации для экономии па-
мяти и ускорения инференса, применяя 4-битную квантизацию BitsAndBytes
для меньших моделей и 2-битную квантизацию AQLM для больших моделей.
Наши результаты подчеркивают важность учета вычислительных затрат
и потребностей в данных при выборе и настройке моделей. Хотя few-shot обу-
чение улучшает производительность моделей для знакомых классов, для более
сложных задач это может быть недостаточно без дальнейшей настройки или до-
полнительного объема данных.