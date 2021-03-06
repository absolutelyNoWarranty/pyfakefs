API Notes
=========

With ``pyfakefs 3.4``, the public API has changed to be PEP-8 conform.
The old API is still supported, and no deprecation warning is issued on usage.
However, if you want to be sure to use the new API, you can add such warnings by using:

.. code:: python

    from pyfakefs.deprecator import Deprecator

    Deprecator.show_warnings = True

In some later version of ``pyfakefs`` we plan to enable the deprecation warnings by default.

Here is a list of selected changes:

:pyfakefs.fake_filesystem.FakeFileSystem:

  CreateFile() -> create_file()

  CreateDirectory() -> create_dir()

  CreateLink() -> create_symlink()

  GetDiskUsage() -> get_disk_usage()

  SetDiskUsage() -> set_disk_usage()

:pyfakefs.fake_filesystem.FakeFile:

  GetSize(), SetSize() -> size (property)

  SetContents() -> set_contents()

  SetATime() -> st_atime (property)

  SetMTime() -> st_mtime (property)

  SetCTime() -> st_ctime (property)
