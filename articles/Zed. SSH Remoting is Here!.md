from:: [Радио-Т 934 — Радио-Т Подкаст](https://radio-t.com/p/2024/11/09/podcast-934/)
url:: [SSH Remoting is Here!](https://zed.dev/blog/remote-development)
on:: 2024-11-12 23:28

Zed has released SSH remoting in beta. Language servers, tasks, and terminals run remotely, UI runs locally. You only specify the SSH host and path in the command line: `zed ssh://host/path`

Zed was built with remote code editing in mind, but supporting SSH was a challenge. They use the ssh's `ControlMaster` setting to maintain a single connection to the host. They download the remote server which can be compiled with `musl`, and this doesn't require dynamic linking, so it can work on older Linux distros and on modern share-noting distros like Nix. 

The remote server is initialized as a daemon, so when connection drops the client can reconnect smoothly. 

Their collab mode is also supported for SSH connections!