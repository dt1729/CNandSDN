History etc: ARPANET(Goal to connect academic computers)

Problems with today's Internet:
1. Running out of addresses: only 2^32 available in total for IPv4 Internet
	1. Allocation should be heirarchial.
	2. Not heirarchial causes over allocation.

2. Congestion control: goal is to match offered load to an available capacity
	1. Does not work well over slow and weak wireless connections
	2. Do not work well on high speed intercontinental paths.

3. Routing: this is how nodes on the internet discover paths.
	1. Today's interdomain routing protocol BGP. Spoiler it's kinda buggy
		1. no security, easily misconfigured,  poor convergence, non-determinism

4. Security: key management is a hassle
5. Denial of Service(DoS): Overload server or network links with unecessary architecture.


[[Internet Design Principles]] http://ccr.sigcomm.org/archive/1995/jan95/ccr-9501-clark.pdf


NAT: Network Address translation? Who does? -> read https://www.rfc-editor.org/rfc/rfc1918.txt

Home network	--- --- ---   NAT  --- --- ---  Public Internet
{Private IP}						{Public IP}(Home router)

Home router makes sure what data to send to what Private IP based on their request.

Does this mean people on internet can't access our PC? No, check out STUN algorithm and DNS from Public Internet into private NAT address.