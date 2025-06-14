# 불용어 제거 (Stopwords Removal)

불용어는 텍스트 분석 시 의미가 없거나 불필요한 단어들을 말합니다. 예를 들어, 영어의 경우 'a', 'the', 'is', 'and' 등이 포함됩니다. TextMiner Pro는 이러한 불용어를 효과적으로 제거하는 기능을 제공합니다.

## 기본 사용법

```python
from textminer import remove_stopwords

# 영어 텍스트에서 불용어 제거
text_en = "This is a sample text with some stopwords"
clean_text_en = remove_stopwords(text_en, lang='english')
print(clean_text_en)
```

## 지원 언어

현재 다음 언어의 불용어 제거를 지원합니다:

- 영어('english')
- 스페인어('spanish')
- 포르투갈어('portuguese')
- 프랑스어('french')
- 이탈리아어('italian')
- 독일어('german')
- 네덜란드어('dutch')
- 러시아어('russian')

## 사용자 정의 불용어

사용자가 직접 불용어 목록을 정의하여 사용할 수도 있습니다:

```python
from textminer import remove_stopwords
from nltk.corpus import stopwords

# 기본 불용어에 사용자 정의 불용어 추가
custom_stopwords = set(stopwords.words('english'))
custom_stopwords.update(['custom', 'words'])

text = "This is a custom text with some custom words"
words = text.split()
clean_words = [w for w in words if w.lower() not in custom_stopwords]
clean_text = ' '.join(clean_words)
print(clean_text)
```

## API 레퍼런스

```python
def remove_stopwords(text: str, lang='english') -> str:
    """
    불용어를 제거하는 함수
    
    Args:
        text (str): 원본 텍스트
        lang (str): 언어 코드 (기본값: 'english')
        
    Returns:
        str: 불용어가 제거된 텍스트
    """
```
