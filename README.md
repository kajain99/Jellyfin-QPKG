# Jellyfin QPKG for QNAP

## What It Is

This is a QPKG package designed to simplify the installation of Jellyfin on QNAP NAS devices. It uses QNAP's Container Station and the official Jellyfin Docker image ([jellyfin/jellyfin](https://hub.docker.com/r/jellyfin/jellyfin)) with the **10.8.10** tag.  Jellyfin is an open-source media server solution that helps you manage and stream your media content seamlessly across devices.This QPKG is built using QNAP's **QDK Kit**, ensuring compatibility with QNAP systems while leveraging the power of Jellyfin's Docker image.

---
## What It Needs

To use this QPKG, you will need:

- A QNAP NAS with **Container Station** installed and configured.
- App Store configured to allow unsigned applications. This QPKG is unsigned because it was created by me, and my public key is not available to the QNAP App Store. Allowing unsigned applications is safe in this case, as long as the QPKG is downloaded from a trusted source. You can review the source code on GitHub to ensure it doesn't contain any harmful settings.

---

## How to Install

### Step 1: Enable Unsigned Package Installation

Since this QPKG is unsigned, you need to allow the installation of unsigned applications:

1. Open your QNAP **App Center**.
2. Navigate to **Settings** > **General**.
3. Check the option **Allow installation of applications without valid signatures**.

### Step 2: Install the QPKG

1. Download the Jellyfin QPKG from [this repository's Releases section](https://github.com/kajain99/Jellyfin-qpkg/releases).
2. In the App Center, click **Install Manually**.
3. Select the downloaded QPKG file and follow the on-screen instructions.

### Step 3: Initial Run

- When you run the application for the first time, all available QNAP shares will be mounted to **`/mnt`**.
- On the first run, you may see the **Select Server** screen. If so:
  - Open a web browser and go to:  
    `http://<your-qnap-ip>:8096/web/#/wizardstart.html`  
    (Replace `<your-qnap-ip>` with your QNAP’s IP address, e.g., `192.168.1.100`.)
  - Follow the on-screen steps to complete the initial setup, including setting your username and password.

---

## Adding Media Libraries

Once Jellyfin is set up, you can easily add your media libraries:

1. Go to the Jellyfin web interface.
2. Navigate to **Add Library**.
3. Select the appropriate folders under **`/mnt`**, where all your QNAP shares are mounted.

---

## Credits

- Built with QNAP's QDK Kit.
- Powered by the official Jellyfin Docker image: [jellyfin/jellyfin](https://hub.docker.com/r/jellyfin/jellyfin).

---

Enjoy your Jellyfin media server on QNAP!
