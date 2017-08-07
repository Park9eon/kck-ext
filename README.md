# KCK
----

**K**orean **C**har **K**otlin Extension

## 개요

한글 초성, 중성, 받침을 분리하거나 한글인지 자음인지 모음인지 검사와 한글에 관련 리스트, 상수를 모아 둡니다.

## 설정법

> $ git clone https://github.com/Park9eon/kck-ext.git

kck-ext/src/com/park9eon/korean/KoreanExtension.kt를 사용!   

## 소개

1. 한글자음 목록

    ```kotlin
    val KOREAN_INITIAL_LIST: List<Char> = listOf('ㄱ','ㄲ','ㄴ','ㄷ','ㄸ','ㄹ','ㅁ','ㅂ','ㅃ','ㅅ','ㅆ','ㅇ','ㅈ','ㅉ','ㅊ','ㅋ','ㅌ','ㅍ','ㅎ')
    ```

2. 한글 모음목록
    
    ```kotlin
    val KOREAN_NEUTRALITY_LIST: List<Char> = listOf('ㅏ','ㅐ','ㅑ','ㅒ','ㅓ','ㅔ','ㅕ','ㅖ','ㅗ','ㅘ','ㅙ','ㅚ','ㅛ','ㅜ','ㅝ','ㅞ','ㅟ','ㅠ','ㅡ','ㅢ','ㅣ')
    ```

3. 한글 받침모음

    ```kotlin
    val KOREAN_SUPPORT_LIST: List<Char?> = listOf(null, 'ㄱ','ㄲ','ㄳ','ㄴ','ㄵ','ㄶ','ㄷ','ㄹ','ㄺ','ㄻ','ㄼ','ㄽ','ㄾ','ㄿ','ㅀ','ㅁ','ㅂ','ㅄ','ㅅ','ㅆ','ㅇ','ㅈ', 'ㅊ','ㅋ','ㅌ','ㅍ','ㅎ')
    ```

    > 받침이 없는 경우도 있기에 0번째는 null입니다.

## 함수

```kotlin
val Char.isKoreanWord: Boolean
```

> 한글 낱말 검사

```kotlin
val Char.isConsonant: Boolean
```

> 자음 검사

```kotlin
val Char.isVowel: Boolean
```

> 모음 검사

```kotlin
val Char.initialOf: Int
```

> 초성 색인

```kotlin
val Char.neutralityOf: Int
```

> 중성 색인

```kotlin
val Char.supportOf: Int
```

> 받침 색인

```kotlin
fun Char.separationKorean(): Triple<Char?, Char?, Char?>
```

> 한글을 분리한다.