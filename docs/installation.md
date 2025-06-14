# 설치 방법

TextMiner Pro는 PyPI를 통해 제공됩니다. `pip` 명령어로 쉽게 설치할 수 있습니다.

```bash
pip install textminer-pro-InjinSung
```

## 필수 요구사항

- Python 3.7 이상
- 다음 패키지가 자동으로 설치됩니다:
  - nltk>=3.8.1
  - scikit-learn>=1.3.2
  - langdetect>=1.0.9

## 수동 설치

GitHub 저장소에서 직접 설치하려면:

```bash
git clone https://github.com/jagari/textminer-pro.git
cd textminer-pro
pip install -e .
```

## NLTK 데이터 다운로드

TextMiner Pro는 처음 실행 시 필요한 NLTK 데이터를 자동으로 다운로드합니다. 
수동으로 다운로드하려면:

```python
import nltk
nltk.download('stopwords')
nltk.download('punkt')
```
