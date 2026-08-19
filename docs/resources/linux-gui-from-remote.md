# Running Linux GUI apps from a remote machine

This is an optional activity. The guide is deliberately minimal. These are the commands I use on a Windows laptop to connect to virtual instance on GCP and display GUI apps.

Assumes VcXsrv, Google Cloud SDK are installed on Windows; and X11 packages are installed on GCP (`sudo apt update && sudo apt install xauth x11-apps`).

## Windows

1. Start **XLaunch**.
2. Choose **Multiple windows**.
3. Set display number to **0**.
4. Choose **Start no client**.
5. Check **Disable access control**.
6. Finish.

## PowerShell

Connect to the GCP VM (use your own instance name and zone):

```powershell
gcloud compute ssh instance-20260819-180758 --zone us-east1-c --ssh-flag="-X"
```

## Debian

Verify X11 forwarding:

```bash
echo $DISPLAY
```

Expected output:

```text
localhost:10.0
```

Launch an X application:

```bash
xclock
```

The clock window should appear on the Windows desktop.


_Acknowledgement: Demo mostly constructed by ChatGPT._