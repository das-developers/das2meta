Orbit files are found here.  For example "junoPJ.dat" contains records
like "2016-10-19T06:10:53.000Z 2016-10-20T06:10:53.000Z 2" which are used
to enumerate and name each Juno interval.

When Autoplot or other Das2 programs are given for a timerange "orbit:junoPJ:2",
Das2 will look for the file https://github.com/das-developers/meta/blob/main/orbits/junoPJ.dat
and then will look up the item "2" to find the corresponding time range.  This
creates a DatumRange object whose "next" version will be "orbit:junoPJ:3", allowing
the scientist to browse data orbit-by-orbit.  (Note ad-hoc orbits files can be
created using orbit:https://example.org/mydata/myintervals.dat:234 where 234 is one
of the identified intervals.)

See also https://das2.org/Orbits, which was the old home for these files.  It is still
checked and is a copy of this location.

Also note this is the Das2 Java code which reads the files: https://github.com/das-developers/das2java/blob/main/dasCoreDatum/src/org/das2/datum/Orbits.java.

## RBSP Orbits
The two orbits files from the Van Allen Probes mission were copied from https://space.physics.uiowa.edu/plasma-wave/rbsp/orbits/.  The
Das2 code still uses these and they are only for reference, until the code is updated.  When this happens, this text should be 
updated.

## PSP Orbits

These were originally committed to [autoplot/orbits](https://github.com/autoplot/orbits/tree/main/psp)
by [Kristoff Paulson](https://github.com/kpaulson) a couple years ago and 
likely need updates.  The upstream source at that time was: 
https://sppgway.jhuapl.edu/psp_data_releases

The Parker Solar Probe files are a copy of files found in [autoplot/orbits](https://github.com/autoplot/orbits/tree/main/psp).  Autoplot still reads these files and the copy here is only for reference.

Jeremy updated 2025 orbits for PSP using https://psp-gateway.jhuapl.edu/website/SciencePlanning/MissionEvents.

## Juno Orbits
Jeremy updates the Juno orbits from the U. Iowa campus, using the Autoplot script /home/jbf/project/juno/git/juno/resources/orbits/createOrbitsFile.jy.  This reads in a .csv file of the Juno_EM2_Ref_Orbital_Useful_for_Science_Planning spreadsheet, which must be converted from .xlsx to .csv.  The
Autoplot script dumps the orbit bounds to the stdout, and these are copied by hand into github.
