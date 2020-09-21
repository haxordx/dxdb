// See the Skipper README on GitHub for usage documentation for `.upload()`, including
// a complete list of options.
req.file('avatar').upload(function (err, uploadedFiles){
  if (err) return res.serverError(err);
  return res.json({
    message: uploadedFiles.length + ' file(s) uploaded successfully!',
    files: uploadedFiles
  });
});
