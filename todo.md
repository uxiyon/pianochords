# Todo list

- [ ] if inkscape is not available, then check if rsvg present, if none present, then send error message on stdout only in case of `--export` use
- [ ] provide a zoom option expressed in percent with `--export`, for instance `--export 250%`
- [ ] reorganize data structure to use note names as array keys
- [ ] offer another way inputing chords: `--realname`, for instance `--realname "Cdim7"` for a C diminished seventh that is auto-calculated
- [ ] offer a `--inversion` option to choose simple inversion (0,1,2,3) with `--realname` option: for instance `--inversion 0` for root position, `--inversion 2` for second inversion
- [x] reorganize triad chords table in order to have only one note change from one to the other
