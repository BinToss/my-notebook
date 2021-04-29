NuGet/Choco Goodness
Choco and NuGet aren't the only package managers…look into how other package manager handle this concept.

0. Important!
	- Verify with Sha1. Use 256 only if necessary.
	- Multiple URL for each package
	- Maintain close relationships with developers to stay up-to-date
	- Allow trustworthy developers to push updates without verification (self-cert)
1. User Support
	- Discord server for support
	- Email for alternative
	- FAQ section on website?
2. Central repo for metadata. Who would host it?
	- Multiple URLs for each package (mirrors)
	- Package payloads are not stored in the repo. 
	- Authors submit various download links which are manually verified by the repo host (until a pseudo-automated system can be created)
	- Manual review is skipped for verified/trusted authors to accelerate update deliveries.
	- Maintain trusting relationships with authors to be accepted by the community.								
3. Miscellaneous
	- How do I manage multiple Halo CE instances? GUID? UUID? Set custom names and allow rename.
	- Should instance detection be handled by the user via file browser and/or user-initiated file system scans for HaloCE.exe/Halo.exe? BOTH
	- should the scan/manual-search require other files to be in the same folder? YES, but which ones?
	- loose integration with chatterbox? (Shared files for update histories and changelogs?)
	- Manual and/or auto check for package updates
	- Toggleable auto-update flag per package