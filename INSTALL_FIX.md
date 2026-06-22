# GayXXX SkyStream install fix

The previous repo parsed, but plugin downloads looped because `dist/plugins.json` pointed to the wrong raw GitHub location (`donatelloroberto/gayxxx/...`).

Fixed URLs now point to:

```text
https://raw.githubusercontent.com/donatelloroberto/gayvn-cs/skystream/dist/<plugin>.sky
```

Use in SkyStream:

```text
https://raw.githubusercontent.com/donatelloroberto/gayvn-cs/skystream/repo.json
```

After pushing, delete the old downloaded plugins in SkyStream, restart SkyStream, then download again.
