#

EVAL_WIN2008R2_X64 ?= http://download.microsoft.com/download/7/5/E/75EC4E54-5B02-42D6-8879-D8D3A25FBEF7/7601.17514.101119-1850_x64fre_server_eval_en-us-GRMSXEVAL_EN_DVD.iso
EVAL_WIN2012R2_X64 ?= http://download.microsoft.com/download/6/2/A/62A76ABB-9990-4EFC-A4FE-C7D698DAEB96/9600.16384.WINBLUE_RTM.130821-1623_X64FRE_SERVER_EVAL_EN-US-IRM_SSS_X64FREE_EN-US_DV5.ISO
EVAL_WIN7_X64      ?= http://care.dlservice.microsoft.com/dl/download/evalx/win7/x64/EN/7600.16385.090713-1255_x64fre_enterprise_en-us_EVAL_Eval_Enterprise-GRMCENXEVAL_EN_DVD.iso
EVAL_WIN81_X64     ?= http://download.microsoft.com/download/B/9/9/B999286E-0A47-406D-8B3D-5B5AD7373A4A/9600.16384.WINBLUE_RTM.130821-1623_X64FRE_ENTERPRISE_EVAL_EN-US-IRM_CENA_X64FREE_EN-US_DV5.ISO

EVAL_WIN2012_X64   ?= http://download.microsoft.com/download/6/D/A/6DAB58BA-F939-451D-9101-7DE07DC09C03/9200.16384.WIN8_RTM.120725-1247_X64FRE_SERVER_EVAL_EN-US-HRM_SSS_X64FREE_EN-US_DV5.ISO
EVAL_WIN7_X32      ?= http://care.dlservice.microsoft.com/dl/download/evalx/win7/x86/EN/7600.16385.090713-1255_x86fre_enterprise_en-us_EVAL_Eval_Enterprise-GRMCENEVAL_EN_DVD.iso
EVAL_WIN81_X32     ?= http://download.microsoft.com/download/B/9/9/B999286E-0A47-406D-8B3D-5B5AD7373A4A/9600.16384.WINBLUE_RTM.130821-1623_X86FRE_ENTERPRISE_EVAL_EN-US-IRM_CENA_X86FREE_EN-US_DV5.ISO
EVAL_WIN8_X64      ?= http://download.microsoft.com/download/5/3/C/53C31ED0-886C-4F81-9A38-F58CE4CE71E8/9200.16384.WIN8_RTM.120725-1247_X64FRE_ENTERPRISE_EVAL_EN-US-HRM_CENA_X64FREE_EN-US_DV5.ISO

EVAL_WIN2008R2_X64_NAME ?= $(shell basename $(EVAL_WIN2008R2_X64))
EVAL_WIN2012R2_X64_NAME ?= $(shell basename $(EVAL_WIN2012R2_X64))
EVAL_WIN7_X64_NAME      ?= $(shell basename ${EVAL_WIN7_X64})
EVAL_WIN81_X64_NAME     ?= $(shell basename $(EVAL_WIN81_X64))

EVAL_WIN2012_X64_NAME   ?= $(shell basename $(EVAL_WIN2012_X64))
EVAL_WIN7_X32_NAME      ?= $(shell basename $(EVAL_WIN7_X32))
EVAL_WIN81_X32_NAME     ?= $(shell basename $(EVAL_WIN81_X32))
EVAL_WIN8_X64_NAME      ?= $(shell basename $(EVAL_WIN8_X64))

WGET ?= wget

.PHONY: isos
isos:	\
	$(EVAL_WIN2008R2_X64_NAME) \
	$(EVAL_WIN2012_X64_NAME) \
	$(EVAL_WIN2012R2_X64_NAME) \
	$(EVAL_WIN7_X32_NAME) \
	$(EVAL_WIN7_X64_NAME) \
	$(EVAL_WIN81_X32_NAME) \
	$(EVAL_WIN81_X64_NAME) \
	$(EVAL_WIN8_X64_NAME)

$(EVAL_WIN2008R2_X64_NAME):
	$(WGET) $(EVAL_WIN2008R2_X64)

$(EVAL_WIN2012_X64_NAME):
	$(WGET) $(EVAL_WIN2012_X64)

$(EVAL_WIN2012R2_X64_NAME):
	$(WGET) $(EVAL_WIN2012R2_X64)

$(EVAL_WIN7_X32_NAME):
	$(WGET) $(EVAL_WIN7_X32)

$(EVAL_WIN7_X64_NAME):
	$(WGET) $(EVAL_WIN7_X64)

$(EVAL_WIN81_X32_NAME):
	$(WGET) $(EVAL_WIN81_X32)

$(EVAL_WIN81_X64_NAME):
	$(WGET) $(EVAL_WIN81_X64)

$(EVAL_WIN8_X64_NAME):
	$(WGET) $(EVAL_WIN8_X64)

.PHONY: hash
hash:
	-rm -f sha1sums.txt.old
	-test -f sha1sums.txt && mv sha1sums.txt sha1sums.txt.old || true
	sha1sum   *.[iI][sS][oO] | tee sha1sums.txt
	#-rm -f md5sums.txt.old
	#-test -f md5sums.txt && mv md5sums.txt md5sums.txt.old || true
	#md5sum    *.[iI][sS][oO] | tee md5sums.txt
	#-rm -f sha256sums.txt.old
	#-test -f sha256sums.txt && mv sha256sums.txt sha256sums.txt.old || true
	#sha256sum *.[iI][sS][oO] | tee sha256sums.txt
