# lsquic
lsquic packaged for zig

# Usage

Update `build.zig.zon`:

```sh
zig fetch --save git+https://github.com/zen-eth/lsquic.git
```

In your `build.zig`:

```zig
    const lsquic_dependency = b.dependency("lsquic", .{
        .target = target,
        .optimize = optimize,
    });

    const lsquic_artifact = lsquic_dependency.artifact("lsquic");
    your_exe.linkLibrary(lsquic_artifact);
```
