# fbtop

fbtop is a simple PHP script for investigating the Filebeat registry.

We could not find any tool that would show us the current state of the Filebeat registry in an easy to read manner. So we wrote one.

The tool is useful for identifying whether filebeat is keeping pace with your logs, and can help indicate whether you have delays in your ingest pipeline.

## Usage

```bash
./fbtop
```

## Options

```
-h --help              Display this help message  
-s --sleep <seconds>   The number of seconds to sleep between updates  
-f --filename <path>   The filebeat registry file to monitor  
-n --noloop            Run once and exit  
```

## Output

The script loops every second and displays an overview of the Filebeat registry.

**Inode**  
The inode number of the log file

**Filename**  
The current filename of the inode

**Filesize**  
The current filesize in bytes

**Offset**  
The current offset in bytes, that filebeat has read up to in the log

**%**  
Percentage of the file read by filebeat

**Rate**  
Estimated rate of bytes read in kb/s

## Requirements

- PHP >= 7.4

## License

MIT License. Please see [LICENSE](LICENSE) for more information.
