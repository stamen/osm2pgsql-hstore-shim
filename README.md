# osm2pgsql-hstore-shim

This is a set of views that allow an `osm2pgsql`
[hstore](http://www.postgresql.org/docs/9.3/static/hstore.html) import to be
used as if it produced a "legacy" schema. It might be handy if you have styles
that you're not quite ready to update the SQL queries for.

This assumes that `osm2pgsql` has been instructed to use a prefix of `hstore`
(`-p hstore`), e.g.:

```bash
osm2pgsql -c -d osm -C4000 -s --number-processes 2 -G -j -S hstore.style --unlogged -p hstore -E 3857 san-francisco.osm.pbf
```
