LoadModule jk_module modules/mod_jk.so
<IfModule mod_jk.c>
# 톰켓 설정 파일 위치
 JkWorkersFile conf.d/workers.properties
# 톰켓 연동시 로그 파일 위치
 JkLogFile logs/mod_jk.log
# 로그내용 래벨 설정
 Jkshmfile run/mod_jk.shm
#로그 내용 설정
 JkLogLevel info
 JkLogStampFormat "[%a %b %d %H:%M:%S %Y]"
 JkOptions +ForwardKeySize +ForwardURICompat -ForwardDirectories
 JkRequestLogFormat "%w %R %V %T %U %q"
</IfModule>
