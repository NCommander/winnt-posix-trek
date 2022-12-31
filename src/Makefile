!include <ntwin32.mak>

C_DEFINES=-DWIN_NT -DSTDC_HEADERS -D_POSIX_SOURCE -DDIRENT -DSTACK_DIRECTION=-1 -D__STDC__ -DDF_POSIX -D_POSIX_ -DCONVERT_TO_SLASHES -UCONVERT_TO_BACKSLASHES
C_INCLUDES=-I..\include\bsd -I..\include\df

all: trek.exe

..\bsdpsx\bsdpsx.lib:
	cd ..\bsdpsx
	nmake
	cd ..\m


trek.exe:  abandon.obj attack.obj autover.obj capture.obj check_out.obj checkcond.obj compkl.obj computer.obj damage.obj damaged.obj dcrept.obj destruct.obj dock.obj dumpgame.obj dumpme.obj dumpssradio.obj events.obj externs.obj getcodi.obj getpar.obj help.obj impulse.obj initquad.obj kill.obj klmove.obj lose.obj lrscan.obj main.obj move.obj nova.obj out.obj phaser.obj play.obj ram.obj ranf.obj rest.obj schedule.obj score.obj setup.obj setwarp.obj shield.obj snova.obj srscan.obj systemname.obj torped.obj utility.obj visual.obj warp.obj win.obj cgetc.obj ..\bsdpsx\bsdpsx.lib
	$(link) $(linkdebug) $(psxflags) -out:$*.exe $** $(psxlibs) ..\bsdpsx\bsdpsx.lib

.c.obj:
	$(cc) $(cflags) $(psxvars) $(cvars) $(cdebug) $(C_DEFINES) $(C_INCLUDES) $*.c
