# Cloudflare R2

Cloudflare R2는 S3의 API와 일부 호환되기 때문에, AWS S3 SDK에서 사용할 수 있습니다.

단, S3 SDK 2.30.x에서는 일치하지 않는 부분이 있어서, 다음과 같은 코드를 추가해야합니다.

```kotlin
S3Client
    .builder()
    // 기존 설정
    .responseChecksumValidation(ResponseChecksumValidation.WHEN_REQUIRED)
    .requestChecksumCalculation(RequestChecksumCalculation.WHEN_REQUIRED)
```
