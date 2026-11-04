# GitHub Archive Downloader

A focused Windows desktop utility for downloading GitHub releases, tags, and branch snapshots into organized ZIP archives.

![GitHub Archive Downloader](assets/GitHubArchiveDownloaderLogo.png)

## What it does

- Enter a GitHub username, `github.com/username`, or a full repository URL.
- Choose a repository from the inline repository list.
- Browse Releases, Tags, or Branches.
- Select one or many versions.
- Download every asset from selected releases.
- Download source archives for selected tags and branches.
- Create a separate, repository-named ZIP for each selected version.
- See current-file details, per-item progress, overall progress, and clear errors.

Public repositories work without authentication. The app uses GitHub's HTTPS API and archive endpoints.

## Download

[Download the latest release](https://github.com/duke2k1/GitHub-Archive-Downloader/releases/latest)

The Windows package is framework-dependent and requires the [.NET 10 Windows Desktop Runtime](https://dotnet.microsoft.com/download/dotnet/10.0).

## How to use

1. Launch GitHub Archive Downloader.
2. Enter a username or repository address and select **Load**.
3. Choose a repository from **Available Repositories**.
4. Select **Releases**, **Tags**, or **Branches**.
5. Check the versions to download.
6. Choose an output folder, then select **Download selected**.

Each selected version is kept separate with a name based on the repository and version, so files from different versions do not overwrite one another.

## Build from source

```powershell
dotnet restore
dotnet publish -c Release --self-contained false /p:UseAppHost=true /p:PublishDir=bin\\Release\\github-archive-downloader\\
```

## Notes

GitHub API rate limits apply to unauthenticated requests. Private repository support and combined all-versions ZIP creation are reserved for future releases.

## Credits

Developed by David Charnock.
