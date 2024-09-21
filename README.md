# MySQL vs PostgreSQL 차이
- MySQL는 무난하게 웹서비스에서 사용하기 용이한 느낌이며 PostgreSQL은 대규모 데이터 서비스에 적합하다.
- [f-lab MySQL vs PostgreSQL 차이](https://f-lab.kr/insight/mysql-vs-postgresql?gad_source=1&gclid=Cj0KCQjwrp-3BhDgARIsAEWJ6Swmudqd9Tc7-UEkrDWxc927kTPxLRg7xZzZCCGRQb3Lb7mttN-IPuoaAms3EALw_wcB)

# Bulk inserting 어떻게 해야 잘했다고 할까?
- SQL 문법에 따라 bulk insert 성능을 개선할 수 있다.
- [Bulk Inserting - MySQL 다량의 데이터 넣기](https://dev.dwer.kr/2020/04/mysql-bulk-inserting.html)
- [[Oracle] 대량 데이터 인서트 하기 (Bulk Data Insert)](https://itsuit.tistory.com/116)

# 옵저버 패턴은 무엇일까?
- 어떤 객체의 상태가 변할 때 그와 연관된 객체 들에게 알림을 보내는 디자인 패턴
  - Observable: 옵저버를 관측하는 객체 `notifyObservers()`로 옵저버에게 상태 변경을 인폼한다.
  - Observer: 상태 변경에 대한 기능 처리를 담당하는 옵저버 객체 일반적으로 `observer`로 처리한다.
- java9에서 `Observable` 인터페이스가 제외 됐다.
  - [java official doc link about this](https://bugs.openjdk.org/browse/JDK-8154801)
  - 서비스 제공보다는 자체 구현이 낫다는 판단
  - Observable이 클래스로 정의되어 있어서 다른 클래스 상속이 불가능
  - 동기화 처리가 안 되어 있어서 Thread-safe 문제가 존재
- [옵저버 패턴이란?](https://pjh3749.tistory.com/266)
