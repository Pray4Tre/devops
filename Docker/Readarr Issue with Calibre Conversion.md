```
2023-09-04 20:35:43.2|Info|IdentificationService|Identifying book 1/1
2023-09-04 20:35:43.6|Info|ImportApprovedBooks|Importing book 1/1 [49179216][Arc of a Scythe, Book 1: Scythe]
2023-09-04 20:35:44.9|Info|ImportApprovedBooks|Importing 1 files
2023-09-04 20:35:50.3|Warn|HttpClient|HTTP Error - Res: HTTP/1.1 [POST] http://calibre:8081/conversion/start/2?library_id=Calibre_Library: 500.InternalServerError (0 bytes)

2023-09-04 20:35:50.3|Warn|ImportApprovedBooks|Couldn't import book /downloads/Scythe - Neal Shusterman.epub

[v0.3.4.2195] NzbDrone.Core.Books.Calibre.CalibreException: Unable to start Calibre conversion: HTTP request failed: [500:InternalServerError] [POST] at [http://calibre:8081/conversion/start/2?library_id=Calibre_Library]
 ---> NzbDrone.Common.Http.HttpException: HTTP request failed: [500:InternalServerError] [POST] at [http://calibre:8081/conversion/start/2?library_id=Calibre_Library]
   at NzbDrone.Common.Http.HttpClient.ExecuteAsync(HttpRequest request) in ./Readarr.Common/Http/HttpClient.cs:line 119
   at NzbDrone.Common.Http.HttpClient.PostAsync[T](HttpRequest request) in ./Readarr.Common/Http/HttpClient.cs:line 369
   at NzbDrone.Common.Http.HttpClient.Post[T](HttpRequest request) in ./Readarr.Common/Http/HttpClient.cs:line 377
   at NzbDrone.Core.Books.Calibre.CalibreProxy.ConvertBook(Int32 calibreId, CalibreConversionOptions options, CalibreSettings settings) in ./Readarr.Core/Books/Calibre/CalibreProxy.cs:line 383

   --- End of inner exception stack trace ---
   at NzbDrone.Core.Books.Calibre.CalibreProxy.ConvertBook(Int32 calibreId, CalibreConversionOptions options, CalibreSettings settings) in ./Readarr.Core/Books/Calibre/CalibreProxy.cs:line 392
   at NzbDrone.Core.Books.Calibre.CalibreProxy.AddAndConvert(BookFile file, CalibreSettings settings) in ./Readarr.Core/Books/Calibre/CalibreProxy.cs:line 120
   at NzbDrone.Core.MediaFiles.UpgradeMediaFileService.UpgradeBookFile(BookFile bookFile, LocalBook localBook, Boolean copyOnly) in ./Readarr.Core/MediaFiles/UpgradeMediaFileService.cs:line 109
   at NzbDrone.Core.MediaFiles.BookImport.ImportApprovedBooks.Import(List`1 decisions, Boolean replaceExisting, DownloadClientItem downloadClientItem, ImportMode importMode) in ./Readarr.Core/MediaFiles/BookImport/ImportApprovedBooks.cs:line 215


2023-09-04 20:37:42.7|Info|ImportListSyncService|Starting Import List Sync
2023-09-04 20:37:42.8|Info|ImportListSyncService|Processing 0 list items
2023-09-04 20:37:42.9|Info|ImportListSyncService|Import List Sync Completed. Items found: 0, Authors added: 0, Books added: 0
```

