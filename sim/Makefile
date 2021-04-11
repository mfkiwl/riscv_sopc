# Makefile for SystemC

export PRJ_PATH=$(shell pwd)/..
export DESIGN=riscv_sopc

all:
	@echo "Verification based on verilator and SystemC"

cmp:
	verilator -Wno-fatal -f ../rtl/filelist/filelist.f --top-module $(DESIGN) --sc --trace --exe sc_main.cpp
	make -C obj_dir -f V$(DESIGN).mk V$(DESIGN)

run:
	./obj_dir/V$(DESIGN)

wave:
	gtkwave wave.vcd &

clean:
	@rm -rf obj_dir wave.vcd

