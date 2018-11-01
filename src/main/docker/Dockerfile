FROM java:8 # 配置运行环境为java 8
VOLUME /tmp # 创建一个临时文件(tomcat需要)
ADD target/wstest.jar app.jar # 添加一个jar包到容器,并命名为app.jar
RUN bash -c 'touch /app.jar' # touch 一下使得它有一个modification time(不重要)
EXPOSE 8080 # 暴露8081端口
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/app.jar"] # 运行