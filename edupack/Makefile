# GNU Make workspace makefile autogenerated by Premake

ifndef config
  config=release_x86_64
endif

ifndef verbose
  SILENT = @
endif

ifeq ($(config),release_x86_64)
  edupack_config = release_x86_64
  BSPLib_1.1.12_34ABD_config = release_x86_64
endif
ifeq ($(config),release_x86)
  edupack_config = release_x86
  BSPLib_1.1.12_34ABD_config = release_x86
endif
ifeq ($(config),debug_x86_64)
  edupack_config = debug_x86_64
  BSPLib_1.1.12_34ABD_config = debug_x86_64
endif
ifeq ($(config),debug_x86)
  edupack_config = debug_x86
  BSPLib_1.1.12_34ABD_config = debug_x86
endif

PROJECTS := edupack BSPLib-1.1.12-34ABD

.PHONY: all clean help $(PROJECTS) Extern Extern/Zefiros-Software Extern/Zefiros-Software/BSPLib

all: $(PROJECTS)

Extern: Extern/Zefiros-Software

Extern/Zefiros-Software: Extern/Zefiros-Software/BSPLib

Extern/Zefiros-Software/BSPLib: BSPLib-1.1.12-34ABD

edupack: BSPLib-1.1.12-34ABD
ifneq (,$(edupack_config))
	@echo "==== Building edupack ($(edupack_config)) ===="
	@${MAKE} --no-print-directory -C . -f edupack.make config=$(edupack_config)
endif

BSPLib-1.1.12-34ABD:
ifneq (,$(BSPLib_1.1.12_34ABD_config))
	@echo "==== Building BSPLib-1.1.12-34ABD ($(BSPLib_1.1.12_34ABD_config)) ===="
	@${MAKE} --no-print-directory -C ../extern/libraries/Zefiros-Software/BSPLib/1.1.12-83ea5/.zpm -f Makefile config=$(BSPLib_1.1.12_34ABD_config)
endif

clean:
	@${MAKE} --no-print-directory -C . -f edupack.make clean
	@${MAKE} --no-print-directory -C ../extern/libraries/Zefiros-Software/BSPLib/1.1.12-83ea5/.zpm -f Makefile clean

help:
	@echo "Usage: make [config=name] [target]"
	@echo ""
	@echo "CONFIGURATIONS:"
	@echo "  release_x86_64"
	@echo "  release_x86"
	@echo "  debug_x86_64"
	@echo "  debug_x86"
	@echo ""
	@echo "TARGETS:"
	@echo "   all (default)"
	@echo "   clean"
	@echo "   edupack"
	@echo "   BSPLib-1.1.12-34ABD"
	@echo ""
	@echo "For more information, see http://industriousone.com/premake/quick-start"