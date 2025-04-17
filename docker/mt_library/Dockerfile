# ベースイメージとして適切な JDK と Maven を使う
FROM --platform=linux/arm64 maven:3.9.5-eclipse-temurin-21
 
# 作業ディレクトリを設定
WORKDIR /app
 
# プロジェクトのファイルをコピー
COPY . .
 
# 必要な依存関係をダウンロードして、プロジェクトをビルド
# RUN mvn clean install
 
# Spring Boot アプリを起動
CMD ["mvn", "spring-boot:run", "-Dspring-boot.run.jvmArguments=-agentlib:jdwp=transport=dt_socket,server=y,suspend=n,address=*:5005"]