This code uses the file_get_contents function to download the file from the URL and file_put_contents to save the file to your server. Note that you need to have write permission to the destination directory on your server.
#
<?php
// URL of the file to download
$file_url = 'http://example.com/file.jpg';

// Destination path on your server to save the file
$destination_path = '/path/to/your/server/uploads/file.jpg';

// Download the file
$file_contents = file_get_contents($file_url);

// Save the file to your server
if(file_put_contents($destination_path, $file_contents)) {
    echo 'File uploaded successfully';
} else {
    echo 'Error uploading file';
}
?>
#
