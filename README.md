# wcet-rs-results
These are the results of tests run by the wcet-rs tool. Each top-level file is a different function analyzed (using the 
-c or -i flag in wcet-rs). Under each top level file, there are different folders for different analyses on the same
function, usually with each one being ran on a different version of the source code, or with different tool flags. 

## Folder structure
Each generally has a similar structure: 

```
/summary.txt: A handwritten summary of the test and what it was trying to accomplish
/out.txt: Terminal output from wcet.rs
/err.txt: Stderr from wcet.rs (sometimes this is just included in /out.txt, or not included at all)
/time.txt: Output from the time linux utility, if the run was being timed
/<board_name/<function_name>: Output from a given function, generated by the wcet-rs tool. Older versions of wcet-rs often produced empty output. 
/<board_name>/summary.txt: Summary produced by wcet-rs tool, often empty because of old versions of the tool 
```

## To Do
- [ ] Make debug output easier to read 
- [ ] Make more of this automated, since a lot of it was created by hand
- [ ] Add git diffs 
