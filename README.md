12/30(목) 오후 3시 Zoom 회의 url : https://us02web.zoom.us/j/4564560061?pwd=cG5mZ1lpV3BHVWJtREZnVExTenR1UT09
모델링: http://www.msaez.io/#/storming/7lxGQRX7nlT2tN40ZhKmJX7Lfrz2/every/79559bcd433a31d6b54d5ffca0f9705b


# 도서대여시스템

Lv2 Intensive Coursework의 일환으로 MSA로 시스템을 구성하기 위한 계획단계부터 분석/설계/구현/운영까지의 프로젝트를 관리함

# 서비스 시나리오

기능적 요구사항
1. 사서가 도서입고처리를 한다(Product)
1. 고객이 도서를 대여신청한다(Order)
1. 고객에게 도서가 배송된다.(Delivery)
1. 도서재고가 차감된다(Product)
1. 고객이 도서를 반납한다.(Order)
1. 도서재고가 증가한다(Product)
1. 고객이 도서대여를 취소한다.(Order, Delivery, Sync))
1. 고객이 MyPage에서 대여현황을 확인한다(View)

비기능적 요구사항

1. 트랜잭션
  1. 고객이 도서대여를 취소하면 반드시 도서배송이 취소되어야한다.(Order, Delivery, Sync))
1. 장애격리
  1. 차감전 도서재고가 없을시 배송과 주문이 취소되어야 한다(Saga pattern)
1. 성능
  1. 도서대여상태가 바뀔때마다 MyPage에서 확인가능해야함
