# fbtop

fbtop is a simple PHP script for investigating the Filebeat registry.

We could not find any tool that would show us the current state of the Filebeat registry in an easy to read manner. So we wrote one.

The tool is useful for identifying whether filebeat is keeping pace with your logs, and can help indicate whether you have delays in your ingest pipeline.

## Usage

```bash
/fbtop
```

N.B. If your filebeat is running in a non-standard location, you may need to modify the path to the registry file in the script.

## Output

The script loops every second and displays an overview of the Filebeat registry.

**Inode**  
The inode number of the log file

**Filename**  
The current filename of the inode

**Filesize**  
The current filesize in bytes

**Offset**  
The current offset that filebeat has read in the log

**%**  
Filebeat percentage of the file read

**Rate**  
The rate of bytes read since the last check in kb/s

## Requirements

- PHP >= 7.4

## License

MIT License. Please see [LICENSE](LICENSE) for more information.