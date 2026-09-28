# Types of Cloud Storage

| | Block Storage | File Storage | Object Storage |
|---|---|---|---|
| **Description** | Data is chopped into equal-sized blocks and stored separately, and the server pulls them together when needed. It works a lot like the hard drive inside a computer. | Data is kept as regular files inside folders and subfolders, and many people or servers can open the same folders over a network. | Every item is saved as an object with its own ID and details (metadata). There are no folders, and you get to it over the web. |
| **Primary Use Case** | Running operating systems and databases, or anything that needs quick, steady performance. | Shared drives and team documents, or any setup where several machines need the same files. | Storing large amounts of files like photos, videos, backups, and logs. |
| **Cloud Provider Example** | AWS EBS (Elastic Block Store) | AWS EFS (Elastic File System) | AWS S3 (Simple Storage Service) |

## Why Object Storage for Your Photos

If your app is going to hold millions of user photos, object storage is the safest bet. Every image is stored as its own object, so as more people upload, you just keep adding more without worrying about disk space or organizing folders. It also isn't tied to your web server container, which disappears when it stops, so your users' photos stay put and can be pulled up online whenever the app asks for them.
