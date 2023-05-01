Orbit files are found here.  For example "junoPJ.dat" contains records
like "2016-10-19T06:10:53.000Z 2016-10-20T06:10:53.000Z 2" which are used
to enumerate and name each Juno interval.

When Autoplot or other Das2 programs are given for a timerange "orbit:junoPJ:2",
Das2 will look for the file https://github.com/das-developers/meta/orbits/junoPJ.dat
and then will look up the item "2" to find the corresponding time range.  This
creates a DatumRange object whose "next" version will be "orbit:junoPJ:3", allowing
the scientist to browse data orbit-by-orbit.  (Note ad-hoc orbits files can be
created using orbit:https://example.org/mydata/myintervals.dat:234 where 234 is one
of the identified intervals.)

See also https://das2.org/Orbits, which was the old home for these files.  It is still
checked and is a copy of this location.
