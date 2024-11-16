# junos-logical-interface-connect-config
## enable logical interfaces

`set chassis fpc 0 pic 0 tunnel-services bandwidth 1g`


## set interfaces ( pair settings )
set logical-systems pe-a-1 interfaces lt-0/0/10 unit 0 description "pe-a-1 to pe-a-2"
set logical-systems pe-a-1 interfaces lt-0/0/10 unit 0 encapsulation ethernet
set logical-systems pe-a-1 interfaces lt-0/0/10 unit 0 peer-unit 1
set logical-systems pe-a-1 interfaces lt-0/0/10 unit 0 family inet address 192.168.10.1/30
set logical-systems pe-a-2 interfaces lt-0/0/10 unit 1 description "pe-a-2 to pe-a-1"
set logical-systems pe-a-2 interfaces lt-0/0/10 unit 1 encapsulation ethernet
set logical-systems pe-a-2 interfaces lt-0/0/10 unit 1 peer-unit 0
set logical-systems pe-a-2 interfaces lt-0/0/10 unit 1 family inet address 192.168.10.2/30

