# LFS

While LFS provides much needed relief for large files (as per its namesake), there is a history of issues in function, and more recently serious vulns such as CVE-2024-53263.  While I'm not advocating completely abandoning LFS, it is a good practice to consider moving large files to a sstandard file service for better resiliency, broader access across systems, atomic paths, and real archive methodologies.  Considering that services like s3 offer region replication, versioning, discrete IAM user controls, object locks (WORM), and data life cycle management, it is well worth choosing s3 for large files in your CI/CD.  After all, for a binary you should change the name, not the contents, and may need access to a very specific version independent of version tags and branches -- not what git does best without added burden.

That said, LFS has advantages for soho, small projects with larger files, and more.
