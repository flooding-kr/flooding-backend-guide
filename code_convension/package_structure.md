# 패키지 구조

백엔드는 큰 틀에서 domain과 global 두 가지로 구성됩니다. domain 내부에는 특정한 관심사(User, Attendance 등)에 따라 여러개의 패키지로 세분화됩니다. global 또한 관심사에 따라 분류되지만, 설정이나 유틸리티와 같이 전역에서 사용하는 것만을 포함한다는 것에서 차이점이 있습니다.
