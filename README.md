Multi-Source P2P File Sharing System

A sophisticated Peer-to-Peer (P2P) file sharing application built with Java, designed for efficient communication and file transfer between devices on a local area network (LAN). This system distinguishes itself by supporting multi-source parallel downloading, allowing files to be fetched in chunks from multiple peers simultaneously.

🚀 Key Features
Multi-Source & Chunk-Based Downloading: Files are split into smaller chunks and downloaded from multiple peers at the same time, significantly increasing transfer speeds.

MD5 Integrity Verification: Uses MD5 hashing to uniquely identify files. This ensures data integrity and allows the system to recognize identical files even if they have different names.

Dynamic Peer Discovery: Implements UDP broadcasting to automatically discover other active peers on the local network without manual IP entry.

Reliable TCP Transfer: Utilizes the TCP protocol for actual file data transmission to ensure error-free and complete delivery of file chunks.

User-Friendly GUI: Features a comprehensive Swing-based interface to monitor download progress, manage shared folders, and view active network peers in real-time.

🛠️ Technical Architecture
The system consists of several core components:

FileServerThread: The server-side module that listens for incoming chunk requests via TCP.

PeerDiscovery: Manages UDP-based node discovery and synchronizes file lists across the network.

DownloadManager & TableModel: Handles the orchestration of active downloads and updates the UI state.

FileShareManager: Responsible for indexing local files and calculating MD5 checksums.

📦 Installation & Setup
Clone the Repository:

Bash
git clone https://github.com/yourusername/p2p-file-sharing.git
Prerequisites:
Ensure you have Java JDK 8 or higher installed on your machine.

Run the Application:
Open the project in your favorite IDE (IntelliJ, Eclipse, VS Code) or run it via terminal:

Bash
java TermProject.P2PApp
📖 How to Use
Establish Connection: Go to Files -> Connect to activate network listeners (uses UDP port 50000 and TCP port 60000).

Configure Folders: Use the "Set Root Shared Folder" and "Set Download Folder" buttons to define your workspace.

Network Scan: Click "Scan Local Network" to find other peers.

Download: Select a file from the remote files list. If the file is hosted by multiple peers, the system will automatically initiate a multi-source download.
