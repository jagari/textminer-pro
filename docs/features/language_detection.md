# 언어 감지 (Language Detection)

TextMiner Pro는 텍스트의 언어를 자동으로 감지하는 기능을 제공합니다. 이 기능은 여러 언어로 작성된 문서를 처리할 때 유용하게 사용될 수 있습니다.

## 기본 사용법

```python
from textminer import detect_language

# 다양한 언어 감지 예제
print(detect_language("This is English text"))  # 'en'
print(detect_language("이것은 한국어 텍스트입니다"))  # 'ko'
print(detect_language("Dies ist deutscher Text"))  # 'de'
print(detect_language("Это русский текст"))  # 'ru'
print(detect_language("これは日本語のテキストです"))  # 'ja'
print(detect_language("这是中文文本"))  # 'zh-cn'
```

## 지원 언어

TextMiner Pro는 langdetect 라이브러리를 기반으로 55개 이상의 언어를 감지할 수 있습니다. 주요 지원 언어에는 다음이 포함됩니다:

- 영어(en)
- 한국어(ko)
- 일본어(ja)
- 중국어(zh-cn, zh-tw)
- 독일어(de)
- 프랑스어(fr)
- 스페인어(es)
- 러시아어(ru)
- 이탈리아어(it)
- 포르투갈어(pt)
- 아랍어(ar)
- 그 외 다수 언어

## 정확도 향상을 위한 팁

1. **충분한 텍스트 제공**: 짧은 텍스트보다는 긴 텍스트에서 더 정확한 결과를 얻을 수 있습니다.
2. **언어 혼합 주의**: 여러 언어가 혼합된 텍스트는 가장 많은 비중을 차지하는 언어로 감지될 수 있습니다.
3. **비슷한 언어 구분**: 예를 들어, 노르웨이어와 덴마크어처럼 비슷한 언어는 구분이 어려울 수 있습니다.

## 언어 코드 형식

반환되는 언어 코드는 ISO 639-1 표준을 따르며, 일부 언어는 지역 코드를 포함합니다(예: 'zh-cn').

## API 레퍼런스

```python
def detect_language(text: str) -> str:
    """
    텍스트의 언어를 감지합니다.
    
    Args:
        text (str): 언어를 감지할 원본 텍스트
        
    Returns:
        str: ISO 639-1 표준의 언어 코드
    """
```
