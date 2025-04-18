# Congestion Control Comparison using Pantheon

This project involves setting up and comparing three congestion control algorithms — **Cubic**, **BBR**, and **Vegas** — using the Pantheon framework. We simulate different network conditions to analyze their performance.

## Algorithms Tested
- **Cubic**: Linux default loss-based algorithm.
- **BBR (Bottleneck Bandwidth and Round-trip propagation time)**: Model-based algorithm by Google.
- **Vegas**: Delay-based algorithm that targets specific RTTs.

## System Requirements
- Ubuntu-based system
- Python 2.7 (not pre-installed on modern systems)
- Git, build tools, and essential dependencies

---

## Installation Steps

### 1. System Update and Dependencies

sudo apt update && sudo apt upgrade -y
sudo apt install -y build-essential dkms linux-headers-$(uname -r)
sudo apt install -y zlib1g-dev libncurses5-dev libgdbm-dev libnss3-dev \
libssl-dev libreadline-dev libffi-dev wget

### 2. Install Python 2.7

### 3. Install pip for Python 2.7

### 4. Pantheon Setup

  Clone Pantheon and install dependencies
       git clone https://github.com/StanfordSNR/pantheon.git
       git submodule update --init --recursive
 Clone and Install MahiMahi
       git clone https://github.com/ravinet/mahimahi.git
      cd mahimahi
      sudo apt install -y libxcb-xinerama0 libpangocairo-1.0-0
      sudo apt install -y libprotobuf-dev protobuf-compiler libhttp-parser-dev \
      libalglib-dev libcap-dev libnl-3-dev libnl-genl-3-dev libnl-route-3-dev \
      apache2 apache2-dev libxcb-present0 libxcb-present-dev \
      libpango1.0-dev libcairo2-dev libgtk2.0-dev libx11-dev
      ./autogen.sh
      ./configure
      make
      sudo make install

### 5. Run Experiments
   Enable IP forwarding
       sudo sysctl -w net.ipv4.ip_forward=1
   Install Pantheon Dependencies

### 6. Run Tests
   python src/experiments/test.py local --schemes "cubic bbr vegas"

### 7. Generating the traces 

### 8. Pushing Results to GitHub
   git config --global user.name
   git config --global user.email
   git clone "new-repo"
   git init
   git remote add origin "path"
   git add. 
   git push (using SSH key)
