# D-day 위젯 (노션 임베드용)

노션에 `/임베드`로 넣는 디데이 위젯입니다. 페이지를 열 때마다 오늘 날짜 기준으로 디데이를 다시 계산합니다.

## 주소 만드는 법

```
https://tabunokiss.github.io/D-day-widget/dday?데이터키=값&데이터키=값
```

물음표(`?`) 뒤에 `데이터키=값`을 넣고, 여러 개는 `&`로 이어 줍니다.

| 데이터 키 | 설명 | 필수 | 기본값 |
|---|---|---|---|
| `date` | 디데이 날짜 (`YYYYMMDD`) | O | |
| `content` | 디데이 내용 (공백은 `%20`) | X | |
| `text` | 글자색 (HEX, 예: `000000`) | X | 라이트 #000 / 다크 #FFF |
| `background` | 배경색 (HEX, 예: `FFFFFF`) | X | 라이트 #FFF / 다크 #191919 |

- 색상은 `#` 없이 써도 되고, 3자리(`FFF`)도 됩니다.
- 배경색만 넣으면 글자색은 배경 밝기에 맞춰 검정/흰색으로 자동 선택됩니다.
- 날짜가 지나면 `D+N`, 당일은 `D-DAY`로 표시됩니다.

## 예시

```
https://tabunokiss.github.io/D-day-widget/dday?content=마무리%20잘하기&date=20261231
https://tabunokiss.github.io/D-day-widget/dday?content=마무리%20잘하기&date=20261231&background=CFFF00
https://tabunokiss.github.io/D-day-widget/dday?content=BIRTHDAY%F0%9F%8E%82&date=20270507&text=C8C8C8
```

## 노션에 두 개를 나란히 넣기

1. 노션에서 `/임베드`로 첫 번째 주소를 넣습니다.
2. 두 번째 임베드를 넣고, 블록 왼쪽 손잡이(⋮⋮)를 끌어 첫 번째 임베드 **오른쪽**에 놓으면 같은 줄 2단이 됩니다.
3. 임베드 모서리를 끌어 크기를 맞춥니다. 글자 크기는 위젯 크기에 맞춰 자동으로 바뀝니다.
