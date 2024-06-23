**Tags**: #nushell #productivity #vs-code #terminal #front-end

# Unix philosophy of shells

## Package Name: Nushell

Link:  [[https://www.nushell.sh/book/installation.html]]

### What is Nu ?:
The Nushell project aims to merge the Unix shell philosophy of connecting simple commands with the modern style of development. It combines the features of a shell and a programming language into a single package. Nushell draws inspiration from various sources such as traditional shells like bash, object-based shells like PowerShell, gradually typed languages like TypeScript, functional programming, and systems programming. Instead of trying to cover every aspect, Nushell focuses on excelling in specific areas.

### Installation Steps Windows :
- **winget**: ```winget install nushell```

- **chocolatey**: ```choco install nushell```

- **scoop**: ```scoop install nu```

- **npm**: ```npm install -g nushell```


### Configuration:
   If needed profile for terminal -  set in settings.json 
   
   ![image](https://github.com/SaileshBK/Notes/assets/101400043/4acb2cbe-8845-4175-a1eb-a567b51768b0)

### Tips and Troubleshooting:
- Easy to set aliases - config command is useful to set aliases 
```config nu```

![image](https://github.com/SaileshBK/Notes/assets/101400043/24dc8351-516e-40ec-8b81-374eab209929)


# Aliases 

# list aliases
alias aliases = help aliases

# Nu config
alias config = config nu

# Run angular
alias nrs = npm run start

# FuzzyFinder for Current project files 
alias fuzzy = fzf --preview 'bat --color=always {}' --bind 'enter:execute(cursor {})'


# Shell Wrappers

def --env yy [...args] {
	let tmp = (mktemp -t "yazi-cwd.XXXXXX")
	yazi ...$args --cwd-file $tmp
	let cwd = (open $tmp)
	if $cwd != "" and $cwd != $env.PWD {
		cd $cwd
	}
	rm -fp $tmp
}

# Setting environment variables 

$env.YAZI_FILE_ONE = "C:/Program Files/Git/usr/bin/file.exe"
