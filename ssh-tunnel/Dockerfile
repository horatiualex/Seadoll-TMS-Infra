FROM alpine:3.21
RUN apk add --no-cache openssh-client sshpass netcat-openbsd
ENTRYPOINT ["sh", "-c", "sshpass -p \"$SSH_PASSWORD\" ssh -o StrictHostKeyChecking=no -o ServerAliveInterval=30 -o ServerAliveCountMax=3 -N -L 0.0.0.0:3306:127.0.0.1:3306 root@$SSH_HOST"]
