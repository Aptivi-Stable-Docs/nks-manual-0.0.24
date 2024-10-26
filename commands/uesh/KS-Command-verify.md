## verify command

### Summary

Verifies the file

### Description

If you've previously calculated the hash sum of a file using the supported algorithms, and you have the expected hash or file that contains the hashes list, you can use this command to verify the sanity of the file.

It can handle three types:

- It can verify files by comparing expected hash with the actual hash.
- It can verify files by opening the hashes file that `sumfiles` generated and finding the hash of the file.
- It can verify files by opening the hashes file that some other tool generated and finding the hash of the file, assuming that it's in this format:
  * `<expected hash>  <file name>`

If the hashes match, that means that the file is not corrupted. However, if they don't match, the file is corrupted and must be redownloaded.

If you run across a hash file that `verify` can't parse, feel free to post an issue or make a PR.

### Command usage

* `verify <algorithm> <calculatedhash> <hashfile/expectedhash> <file>`

### Examples

* `verify MD5 73470a9f4e1c36bed24a658e47104c77 73470a9f4e1c36bed24a658e47104c77 TealerOS.ppsm`: Verifies the two MD5 sums for a PowerPoint macro-enabled slideshow.
* `sumfile SHA256 c6e7bdada5a04a639e745b41ea43ae36b796b4cf4128e3dcb3c2502ab034caa3 SHA256SUMS debian-10.6.0-i386-netinst.iso`: Verifies the SHA256 sum of the Debian netinst iso using the SHA256SUMS file generated by tools other than KS.