# General Instructions
Files that may be invisible/excluded to Copilot Chat (treat as unavailable)

When you're working in any repo, assume the following files/folders may be **excluded from Copilot Chat context** (even if they exist locally or are under git control). Don't ask users to paste them, don't rely on their contents, and never suggest committing secrets.

If you need values typically stored in these files, prefer **IaC variables**, **Secret Manager**, or **environment variables** configured in deployment tooling.

Example exclusion patterns:

```yaml
"*":
  # Environment files
  - "*.env"
  - "*.env.local"
  - ".env.*.local"

  # Keys and certificates
  - "*.key"
  - "*.pem"
  - "*.crt"
  - "*.p12"
  - "*.jks"

  # Configurations with secrets
  - "config.json"
  - "credentials.json"
  - "secrets.yml"
  - "access_tokens.json"
  - "*.passwords"
  - "*.private"
  - "*.secret"

  # IDE and editor files
  - "*.sublime-project"
  - "*.sublime-workspace"
  - "*.vscode/"
  - ".idea/"

  # Node.js and package files
  - "node_modules/"
  - "bower_components/"

  # Logs
  - "*.log"
  - "*.out"
  - "*.err"
  - "npm-debug.log*"
  - "yarn-debug.log*"
  - "yarn-error.log*"

  # Build and dist files
  - "dist/"
  - "build/"
  - "public/"
  - "*.tar.gz"
  - "*.zip"
  - "*.rar"
  - "*.7z"
  - "*.tgz"

  # Backup and swap files
  - "*.bak"
  - "*.swp"
  - "*.swo"
  - "*~"
  - "Thumbs.db"
  - "Desktop.ini"

  # Database files
  - "*.db"
  - "*.db-backup"

  # Java files and builds
  - "*.class"
  - "*.jar"
  - "*.war"
  - "*.ear"
  - "*.swm"

  # Coverage reports
  - "coverage/"

  # Windows specific files
  - "*.cab"
  - "*.msi"
  - "*.exe"

  # macOS specific files
  - ".DS_Store"

  # Linux specific files
  - "*.swp"

  # Terraform files
  - "*.tfstate"
  - "*.tfstate.*"
  - "*.tfvars"
  - "*.tfvars.json"
  - ".terraform/"

  # Ignore Terraform plan files
  - "*.plan"
```
