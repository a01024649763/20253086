# 20253086
Study of Linux commands: top, ps, jobs, kill
🧑‍💻 Linux Process Commands Study

리눅스 프로세스 관련 명령어 top · ps · jobs · kill 정리 문서입니다.
다양한 Markdown 기능을 사용하였습니다.

📌 목차

1. top

2. ps

3. jobs

4. kill

5. 명령어 비교 테이블

6. 참고 자료

1. top
✔ 개요

top은 리눅스 시스템의 실시간 프로세스 및 자원 사용 상태를 모니터링하는 명령어입니다.

✔ 특징

CPU / 메모리 사용량 실시간 확인

프로세스 우선순위 수정 가능

P → CPU 사용량 순 정렬

M → 메모리 사용량 순 정렬

✔ 사용 예시
top

✔ 실행 화면 예시
<img width="2292" height="1309" alt="화면 캡처 2025-11-30 000129" src="https://github.com/user-attachments/assets/0cf2a878-c15f-49df-957e-03b039c263f7" />

2. ps
✔ 개요

ps는 프로세스 상태(Process Status) 를 스냅샷 형태로 출력합니다.

✔ 자주 사용하는 옵션
옵션	설명
ps	현재 셸의 프로세스
ps -e	시스템 전체 프로세스
ps -f	자세한 정보 표시
ps aux	모든 프로세스 출력 (가장 많이 사용)
✔ 사용 예시
ps aux
ps -ef

3. jobs
✔ 개요

jobs는 현재 셸에서 실행 중인 백그라운드 작업 목록을 보여줍니다.

✔ 관련 명령어

& → 백그라운드 실행

Ctrl + Z → 실행 중 작업 일시정지

bg → 백그라운드로 재개

fg → 포그라운드로 가져오기

✔ 사용 예시
jobs

4. kill
✔ 개요

kill은 특정 프로세스에 종료 신호(Signal) 를 보내는 명령어입니다.

✔ 자주 사용되는 Signal
번호	이름	설명
15	SIGTERM	정상 종료 요청 (기본값)
9	SIGKILL	강제 종료
2	SIGINT	인터럽트 (Ctrl + C)
✔ 사용 예시
kill 1234
kill -9 1234

5. 명령어 비교 테이블
명령어	실시간	목적	대표 기능
top	✔	전체 시스템 모니터링	CPU/메모리 실시간 확인
ps	✖	프로세스 정보 출력	aux, -ef
jobs	✔	백그라운드 작업 확인	bg, fg
kill	✖	프로세스 종료	-9, SIGTERM
6. 참고 자료

https://man7.org/linux/man-pages/man1/top.1.html

https://man7.org/linux/man-pages/man1/ps.1.html

https://man7.org/linux/man-pages/man1/kill.1.html
