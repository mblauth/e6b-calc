all: MBIN.raw INMB.raw KTKMH.raw KMHKT.raw PTHMS.raw DST.raw

%.raw: %.txt
	cat $< | comp41 >$@

clean:
	rm -f *.raw
