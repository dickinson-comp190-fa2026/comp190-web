# Homework assignment HW1

## Homework log

Remember to create a new post with a new topic "HW1" in your homework log channel on Microsoft Teams. Make a reply to that topic whenever do some work on this assignment. You can also post questions there. Your posts should provide evidence that you spent several hours doing meaningful work.

## Objectives

The main objective for this assignment is to spend time familiarizing yourself with a Linux environment that you can either install or access from your own computer. You can use as much AI help as desired for this without needing to acknowledge or mention it. At a minimum you need to have shell access to your Linux environment (that is, you are able to run commands in a terminal window). You can use either a local installation of Linux, or a virtual machine (VM) running Linux, or a remote Linux server that you can access via SSH. On Windows, the easiest way to access a Linux environment is to use the Windows Subsystem for Linux (WSL). On macOS, you can try Multipass.

### Cloud-based option

Instead of running a local installation of Linux, you can use a cloud-based Linux environment such as Google Cloud Platform (GCP), Amazon Web Services (AWS), or Microsoft Azure. 

If you're looking for a specific suggestion, here is a quick, inexpensive way to create a Linux box on GCP via the [Google Cloud Console](https://console.cloud.google.com/):
1. Navigate to **Compute Engine** > **VM Instances** in the GCP Console.
2. Click **Create Instance**.
3. **Region / Zone:** Select `us-central1` (Iowa) or `us-east1` (South Carolina).
4. **Machine Configuration:**
   * **Machine family:** General-purpose
   * **Series:** E2
   * **Machine type:** `e2-micro`
5. **Boot Disk:** Leave as **Debian**.
6. Click **Create**.
_Acknowledgement: the above instructions were provided by Google Gemini._

## PB version

The Professor Braught version is available as:
* [01-A-OSandLinux.docx](../materials/01-A-OSandLinux.docx)
You are free to follow this version closely if desired, or use it as a loose guide to your activities.

## Likely quiz questions

* What is Linux?
* What is Unix?
* In 1-2 sentences, describe one way that you have accessed a Linux operating system from a computer running either Windows or macOS.
* What two commands would you use in a Linux terminal to (i) change to your home directory, and then (ii) list all files in that directory, including files that are usually hidden?