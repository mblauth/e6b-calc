all: MBIN.raw INMB.raw KTKMH.raw KMHKT.raw

%.raw: %.txt
	cat $< | comp41 >$@

clean:
	rm -f *.raw
