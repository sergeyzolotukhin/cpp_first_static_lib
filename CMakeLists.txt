cmake_minimum_required(VERSION 3.15)
project(pdcurses C)

set(CMAKE_C_STANDARD 11)
add_definitions(-DPDCDEBUG)

include_directories(.)
include_directories(common)
include_directories(wincon)

add_library(pdcurses
        common/acs437.h
        common/acsgr.h
        common/acsuni.h
        common/font437.h
        common/iconbmp.h
        pdcurses/addch.c
        pdcurses/addchstr.c
        pdcurses/addstr.c
        pdcurses/attr.c
        pdcurses/beep.c
        pdcurses/bkgd.c
        pdcurses/border.c
        pdcurses/clear.c
        pdcurses/color.c
        pdcurses/debug.c
        pdcurses/delch.c
        pdcurses/deleteln.c
        pdcurses/getch.c
        pdcurses/getstr.c
        pdcurses/getyx.c
        pdcurses/inch.c
        pdcurses/inchstr.c
        pdcurses/initscr.c
        pdcurses/inopts.c
        pdcurses/insch.c
        pdcurses/insstr.c
        pdcurses/instr.c
        pdcurses/kernel.c
        pdcurses/keyname.c
        pdcurses/mouse.c
        pdcurses/move.c
        pdcurses/outopts.c
        pdcurses/overlay.c
        pdcurses/pad.c
        pdcurses/panel.c
        pdcurses/printw.c
        pdcurses/refresh.c
        pdcurses/scanw.c
        pdcurses/scr_dump.c
        pdcurses/scroll.c
        pdcurses/slk.c
        pdcurses/termattr.c
        pdcurses/touch.c
        pdcurses/util.c
        pdcurses/window.c
        wincon/pdcclip.c
        wincon/pdcdisp.c
        wincon/pdcgetsc.c
        wincon/pdckbd.c
        wincon/pdcscrn.c
        wincon/pdcsetsc.c
        wincon/pdcutil.c
        wincon/pdcwin.h
        curses.h
        curspriv.h
        panel.h)
