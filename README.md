Python script that calculates pentanomial elo ratings of chess engines/players in a tournament using a similar methodology to [Ordo](https://github.com/michiguel/Ordo).
How to use:
- Required python dependencies: scipy
- Run the command: `python calculateratings.py --pgnfile FILE` or `python calculateratings.py --pgnfile FILE1 FILE2 FILE3 ...` for multiple PGN's.
- To set the number of simulations, add `--simulations NUM` with the default being 1000.
- To set the seed for the random number generator, you can add `--rngseed SEED` with the default seed being 42.
- To set the average rating for the pool, use the argument `--average AVG` with the default being 2300.
- If you want to set an anchor engine, use the argument `--anchor ENGINE`.
- To set the number of parallel processes, set `--concurrency N` with the default being the number of CPU hardware threads.
- For the number of simulations the recommended minimum amount is 1000, although the higher the more accurate the error bar becomes.
- This script only works for tournaments where games are played in pairs where each player swaps colors.
- PGNs must be correctly formatted where every unique gamepair has a unique "Round" PGN header tag. So for example if a PGN has 100 games then the "Round" tag must be incremented from 1 to 50 for every gamepair.
