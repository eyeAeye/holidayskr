# holidayskr

<div align="center">

![holidayskr logo](https://yoonminlee-blog-image.s3.ap-northeast-2.amazonaws.com/holidayskr.png)

[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2F6mini%2Fholidayskr&count_bg=%235A81D4&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false)](https://hits.seeyoufarm.com)

</div>

대한민국의 공식 휴일을 계산하는 Python 패키지입니다. 양력 및 음력에 기반한 고정 휴일 뿐만 아니라, 매년 변동되는 휴일(대체 공휴일, 선거일 등)까지 포함하여 정확한 휴일 정보를 제공합니다. 금일 혹은 특정 날짜가 휴일인지 확인하거나, 주어진 연도의 모든 휴일을 조회할 수 있습니다. 이를 통해 개인 및 기업 사용자는 휴일에 관련된 계획을 더욱 효과적으로 수립할 수 있습니다.

## 주요 기능

- **휴일 확인**: 특정 날짜가 대한민국의 공휴일인지 여부를 확인합니다. 이는 어린이날, 설날, 추석 등의 공휴일 뿐만 아니라 선거일과 같은 특별한 날짜도 포함합니다.
- **연간 휴일 조회**: 지정한 연도의 모든 공휴일을 조회합니다. 이 기능을 통해 사용자는 한 해 동안의 모든 공휴일을 미리 알 수 있으며, 계획을 세울 때 유용하게 사용할 수 있습니다.
- **양력 및 음력 휴일 지원**: 양력과 음력에 기반한 공휴일을 모두 지원합니다. 음력 휴일인 설날과 추석은 물론, 석가탄신일과 같은 중요한 날짜를 양력으로 변환하여 제공합니다.
- **대체 휴일 포함**: 주말과 겹치는 공휴일에 대한 대체 공휴일 정보를 제공합니다. 대체 공휴일 정책에 따라 변경되는 휴일 정보를 정확히 반영합니다.
- **선거일 지원**: 대통령 선거, 국회의원 선거, 지방 선거 등 주요 선거일을 포함하여, 선거일이 공휴일로 지정될 경우 이를 확인할 수 있습니다. 선거일이 공휴일로 지정되는 연도에는 자동으로 해당 정보를 포함하여 사용자에게 제공합니다.


## 설치 방법

이 패키지를 사용하기 위해 Python 3.6 이상이 필요합니다. 다음 명령어를 통해 설치할 수 있습니다:

```bash
pip install holidayskr
```

## 사용 예제

### 특정 날짜가 휴일인지 확인하기

```python
from holidayskr import is_holiday

# 어린이날 확인하기
if is_holiday('2024-05-05'):
    print("2024년 5월 5일은 휴일입니다.")
else:
    print("2024년 5월 5일은 휴일이 아닙니다.")
```

### 오늘 날짜가 휴일인지 확인하기

```py
from holidayskr import today_is_holiday

# 오늘 날짜 휴일 확인
if today_is_holiday():
    print("오늘은 휴일입니다.")
else:
    print("오늘은 휴일이 아닙니다.")
```

### 지정한 연도의 모든 휴일 조회하기

```py
from holidayskr import year_holidays

# 2024년의 모든 휴일 조회
holidays = year_holidays('2024')
for holiday in holidays:
    print(holiday.strftime('%Y-%m-%d'))
```

## 개발 배경

대한민국의 휴일은 양력 고정 휴일, 음력 휴일, 그리고 매년 달라지는 대체 공휴일로 구성되어 복잡합니다. 이로 인해 개발자들이 휴일 관련 계산을 할 때 많은 시간을 소비하게 됩니다. holidayskr 패키지는 이러한 계산을 간단하게 해결하여, 개발자들이 보다 중요한 기능 개발에 집중할 수 있도록 돕고자 합니다.

## 기여하기

holidayskr 프로젝트는 오픈 소스 커뮤니티에 기여하고자 하는 모든 분들을 환영합니다. 프로젝트에 기여하는 방법은 다양하며, 버그 신고, 기능 제안, 문서 개선 뿐만 아니라 새로운 휴일 정보의 추가나 기존 휴일 정보의 수정 등이 포함됩니다.

- **버그 신고**: 사용 중 발견한 버그를 GitHub 이슈로 신고해 주세요.
- **기능 제안**: 새로운 기능에 대한 아이디어가 있다면 이슈를 통해 제안해 주세요.
- **문서 개선**: 프로젝트 문서를 개선하는 데 기여할 수 있습니다. 사용자 가이드, 설치 안내, 예제 등의 문서를 개선하여 더 많은 사람이 쉽게 사용할 수 있도록 도와주세요.
- **휴일 정보 업데이트**: 대한민국의 공휴일은 변동될 수 있으며, 새로운 휴일이 생길 수도 있습니다. 변동되거나 새로 생긴 휴일 정보에 대해 알고 있다면, 해당 정보를 프로젝트에 반영할 수 있도록 Pull Request(PR)를 해주세요.

## 라이선스

holidayskr는 MIT 라이선스 하에 배포됩니다. 자세한 내용은 LICENSE 파일을 참조해 주세요.

## 연락처

- 이메일: real6mini@gmail.com
- 블로그: https://yoonminlee.com
- GitHub: https://github.com/6mini/holidayskr