# Todo list

- [x] if inkscape is not available, then check if rsvg present, if none present, then send error message on stdout only in case of `--export` use
- [x] provide a zoom option, for instance `--zoom 2.0`
- [x] reorganize data structure to use note names as array keys
- [x] improve chord input mode by removing --chord option
- [x] improve stream mode by removing --stream option
- [ ] provide ascii output as a convenient fast feature
- [ ] provide another way inputing chords: `--realname`, for instance `--realname "Cdim7"` for a C diminished seventh that is auto-calculated
- [ ] provide a `--inversion` option to choose simple inversion (0,1,2,3) with `--realname` option: for instance `--inversion 0` for root position, `--inversion 2` for second inversion
- [x] reorganize triad chords table in order to have only one note change from one to the other
