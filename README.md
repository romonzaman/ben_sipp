# ben_sipp

##dependancy - debian
```
apt-get install gcc ncurses ncurses-dev make autoconf build-essential g++
```
## install
```
git clone https://github.com/romonzaman/ben_sipp.git
cd sipp_3.5.0
bash build.sh

cp sipp_3.5.0/sipp .
```

## command to run test
```
sipp -inf user2.csv -sf uac_auth.xml -r cps -rp rate_period -l call_limit -d call_duration -s target_phonenumber -i local_ip  server_IP

-inf = user file
-sf = sip mode and profile
-r = call rate
-rp = call rate period (in milisec)
-l = limit call
-d = call duration (in milisecond)
-s = target phonenumber
-i = local ip through which call made
```

### for example,
we like to dial 442071833026 @ 178.62.76.107 (with call duration 5000msecond) at 10 cps  by call limt 10
using local ip,10.0.0.100  
```
sipp -inf user2.csv -sf uac_auth.xml -r 10 -rp 1000 -l 20 -d 5000 -s 442071833026 -i 10.0.0.100 178.62.76.107
```
