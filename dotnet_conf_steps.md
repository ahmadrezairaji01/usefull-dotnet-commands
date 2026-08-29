**Steps to install .NET SDKs:**
 
```
rm -rf "$HOME/.dotnet"
```

```
mkdir -p "$HOME/.dotnet"
```

```
curl -L https://dot.net/v1/dotnet-install.sh -o /tmp/dotnet-install.sh
```

```
chmod +x /tmp/dotnet-install.sh
```

```
/tmp/dotnet-install.sh --channel 6.0 --install-dir "$HOME/.dotnet"
```

```
/tmp/dotnet-install.sh --channel 8.0 --install-dir "$HOME/.dotnet"
```

```
/tmp/dotnet-install.sh --channel 10.0 --install-dir "$HOME/.dotnet"
```

```
cat >> ~/.bashrc <<'EOF'
```
```
export DOTNET_ROOT="$HOME/.dotnet"
export PATH="$DOTNET_ROOT:$DOTNET_ROOT/tools:$PATH"
EOF
```

```
source ~/.bashrc
```

**To use an SDK for a project**
```
dotnet new globaljson --sdk-version 8.0.423
```


**To restore dotnet tools:**

```
dotnet new tool-manifest
```

```
dotnet tool install dotnet-ef --version 8.*
```

```
dotnet tool restore
```

**Migrations:**
```
dotnet ef migrations add InitialCreate
```

```
dotnet ef database update
```
