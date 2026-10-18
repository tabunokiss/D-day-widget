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

## 위젯 여러 개를 한 줄에 넣기 (최대 4개)

노션은 한 열 안에 다시 열을 만들 수 없어서, 임베드를 따로 넣으면 같은 줄에 놓을 수 없습니다.
대신 **임베드 하나**에 위젯을 여러 개 넣으면 됩니다. 두 번째부터는 데이터 키 뒤에 번호를 붙입니다.

| 위젯 | 데이터 키 |
|---|---|
| 1번째 | `date`, `content`, `text`, `background` |
| 2번째 | `date2`, `content2`, `text2`, `background2` |
| 3번째 | `date3`, `content3`, `text3`, `background3` |
| 4번째 | `date4`, `content4`, `text4`, `background4` |

```
https://tabunokiss.github.io/D-day-widget/dday/?content=AI%20콘텐츠%20페스티벌&date=20261112&background=D9FF4F&content2=입사&date2=20240902&background2=D8B4FE
```

- 위젯이 2개 이상이면 자동으로 **정사각형**이 되고, 칸 크기에 맞춰 줄어듭니다.
- 위젯 사이 빈 곳은 투명해서 노션 배경이 그대로 보입니다.
- 위젯이 하나일 때도 `&square=1`을 붙이면 정사각형이 됩니다.
