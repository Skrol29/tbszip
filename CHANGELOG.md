# Changes in TbsZip

All notable changes to this project will be documented in this file.

## [2.17] - 2023-09-17

### Enhancements

- PHP 8.2 compatibility 

### Added

- Support URI when the archive to open is a stream resource.

## [2.16] - 2014-04-08

### Fixed

- could not download a file that has the same name as the opened archive.

## [2.15] - 2013-10-15

### Fixed

- Archives with comment can now be opened by TbsZip.

### Enhancements

- Clearer error messages for PHP in CLI mode.
- Clearer error messages for the interconnection with OpenTBS.

## [2.14] - 2013-06-11

### Added

- can open an archive from a PHP file handle

## [2.13] - 2013-04-14

### Added

- new method FileGetState()

## [2.12] - 2013-03-16

### Fixed

-  may produce a corrupted archive when the original was using data descriptors without the signature.

### Enhancements

- new argument $UseIncludePath.
- debug mode is smarter.

## [2.11] - 2011-02-14

    bug fixed: method FileCancelModif() doesn't cancel added files.

## [2.10] - 2011-08-13

### Fixed

- PHP warning "Notice: Undefined variable: AddDataLen..." happens when deleting a file whitout adding any file.

## [2.9] - 2011-07-22

    bug fixed: a minor bug on FileRead when the asked file does not exists.

## [2.8] - 2011-06-08

### Fixed

- PHP warning "Warning: fclose(): 10 is not a valid stream resource" may happen when closing an archive twice.

## [2.7] - 2011-06-07

### Fixed

- PHP error "supplied argument is not a valid stream resource" or "Undefined property: clsOpenTBS::$OutputHandle" may happen when using method Flush().

## [2.6] - 2011-06-07

### Enhancements

- now raise a TbsZip error if Flush() attempts to overwrite a locked file.

## [2.5] - 2011-05-12

### Fixed

- strict compatibility with PHP 5 (no PHP warning with error reporting E_STRICT)

## [2.4] - 2011-03-25

### Fixed

-  the new created archive using Flush() was not unlocked at the end of the flush. The clsTbsZip instance had still an handle on it.

### Enhancements

- now raise a TbsZip error if Flush() attempts to overwrite the current archive.
- property DisplayError is set to true by default.

## [2.3] - 2010-11-29

### Fixed

- an archive created with both methods CreateNew() and Flush(TBSZIP_DOWNLOAD) could be truncated because the final size of the archive was badly estimated.

## [2.2] - 2010-10-28

### Fixed

- some added or modified files can be saved in the archive with a wrong CRC control code. This could make softwares to consider the file or the archive as corrupted. Only few CRC codes are wrongly saved, thus the bug is rare and can seem to appear randomly.

## [2.1] - 2010-07-01

### Fixed

- bug fixed: when adding a new file in the archive, the time of the file was wrong (date was ok)

### Added

- new method CreateNew()

### Enhancements

- TbsZip now changes the date and time of a file in the archive when the file content is replaced