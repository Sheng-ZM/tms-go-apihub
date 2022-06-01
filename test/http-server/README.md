
# fast-http-server
fast-http-server is a service which receives messages from http and handle it.

## how to run
cd test
cd fast-http-server
go build
./fast-http-server -addr="127.0.0.1:6060"


## examples
## ע��
curl -X GET -H 'Content-Type: application/json' -d '{"nonce":"abcd","utc":"1234","checksum":"279fc4ff795c5fb5047c27d9f23f2332"}' "http://localhost:6060/register?app=appid1"
//�ɹ�ע���򷵻� {token:"xxx"��expires:3600}
## ��ʾ
curl -X GET -H "Authorization:tokenstring"'Content-Type: application/json' -d '{"content":"hello world!"}' "http://localhost:6060/echo?app=appid1
//����: {"content":"hello world!"}
## ����
curl -X GET -H "Authorization:tokenstring"'Content-Type: application/json' -d '{"param1":"hello","param2":"world"}' "http://localhost:6060/joint?app=appid1
//����: {"content":"helloworld"}
## ���ݿո�ִ�
curl -X GET -H "Authorization:tokenstring"'Content-Type: application/json' -d '{"content":"hello world"}' "http://localhost:6060/split?app=appid1
//����: {"content":"hello,world"}
