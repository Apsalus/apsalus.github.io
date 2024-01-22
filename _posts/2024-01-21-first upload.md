---
layout: post
title: test upload
date: 2024-01-21 19:34 +0800
last_modified_at: 2024-01-21 20:08:25 +0800
tags: [SpringBoot]
toc:  true
---
스프링 @어노테이션
💡 @Autowired
- 필드, 메서드, 생성자에 사용할 수 있습니다.

- Bean의 타입을 사용해서 주입할 빈 객체를 찾습니다.

- 하나의 인터페이스는 한 개의 클래스로만 구현할 수 있다. (두 개 이상의 클래스가 구현하면 안 됩니다.)

@Service
public class MemberService {

    @Autowired
    private A a;
}
💡 @Resource
- 필드, 메서드에 사용할 수 있다. 생성자에는 사용할 수 없습니다.

- Bean의 이름을 사용해서 주입할 빈 객체를 찾습니다.

@Resource(name = "memberRepository")
private MemberRepository memberRepository;
💡 @Data
@Getter / @Setter, @ToString, @EqualsAndHashCode와 @RequiredArgsConstructor, @Value 를 합쳐놓은 것 이라고 볼 수 있습니다.

💡 @Getter
private로 설정된 필드 변수를 외부에서 접근하려고 만든 것

💡 @Setter
private로 설정된 필드 변수를 외부에서 수정하려고 만든 것

💡 @ToString
객체가 가지고 있는 정보나 값들을 문자열로 만들어 리턴 하는 것

💡 @EqualsAndHashCode
equals()메소드와 hashCode()메소드를 생성해줍니다.

💡 @RequiredArgsConstructor
초기화 되지 않은 final 필드나 @NonNull 어노테이션이 붙은 필드에 대해 생성자를 만들어 줍니다.

++ 비슷한 어노테이션으로 생성자를 만들어주는 어노테이션(@AllArgsConstructor, @NoArgsConstructor)가 있습니다.

💡 @Value
불변한 자바 클래스를 생성할 때 편리하게 사용할 수 있도록 도와줍니다.

💡 @Alias
XML 매핑 파일에서 결과 매핑을 설정할 때, 매핑 대상인 클래스의 이름을 간소화하기 위해 사용됩니다.

💡 @CookieValue
클라이언트가 HTTP 요청을 보낼 때 해당 쿠키가 존재하면 그 값을 cookieValue에 할당하고,
존재하지 않으면 null이 할당됩니다.