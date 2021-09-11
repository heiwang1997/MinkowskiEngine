# Jiahui's fork of MinkowskiEngine

## NOTE

I will work on my master branch, and merge with upstream using the following command.
List all files without untracked ones with `gst -uno`

## Merging with upstream head

1. Commit your changes.
2. `git pull upstream master`
3. Commit the merge.
4. (Optionally) `git push origin master`

## Compile

Or simply do:
```bash
ca
python setup.py install
```

## Modifications compared

`git diff <HEAD@upstream>`

0. Add more cuda flags for more devices for cross-platform usage.
1. Add cuda support for `sparse_quantize`.
2. Revert all changes in Issue 308, that will cause memory leak and slow inference on some machines I have. (Note the original problem in 308 is fixed for pytorch 1.9).
