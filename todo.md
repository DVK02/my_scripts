# Todo Script

- Add colour coding to displayed text
    - Configurable colour schemes
        - Project name
        - Project gap
        - Error message 
    - Take colour codes from an external config file
        - Include catppuccin macchiato by default

# Setup Script

- Create script `setup`
- Add a symbolic/soft link, for each script inside /my_script, inside ~/bin
    - If ~/bin does not exist, create it
- System Configuration (Fedora)
    - DNF (/etc/dnf/dnf.conf)
        ```
        # Improve DNF install speed
        fastestmirror=True
        max_parallel_downloads=10
        defaultyes=True
        keepcache=True
        ```
    - Enable rpm fusion free & nonfree repositories
    - Enable flathub repository
- System Update (Fedora)
    - sudo dnf upgrade --refresh
- Multimedia Support (Fedora + rpm fusion enabled)
    - `sudo dnf swap ffmpeg-free ffmpeg --allowerasing`
    - `sudo dnf groupupdate multimedia --setopt="install_weak_deps=False" --exclude=PackageKit-gstreamer-plugin`
    - `sudo dnf groupupdate sound-and-video`

# Backup Script

- Automate Backups for root and home
