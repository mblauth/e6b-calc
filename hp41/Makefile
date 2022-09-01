all: MBIN.raw INMB.raw

%.raw: %.txt
	cat $< | comp41 >$@

clean:
	rm -f *.raw
